---
title: Advanced Operator Configuration
linkTitle: Advanced Operator Config
weight: 80
description: >
  Learn how to configure the Armory Operator for specialized use cases.
aliases:
  - /docs/installation/armory-operator/op-advanced-config/
---

{{< include "armory-operator/os-operator-blurb.md" >}}

## Custom Halyard configuration

To override Halyard's configuration, create a Kubernetes [ConfigMap](https://kubernetes.io/docs/concepts/configuration/configmap/) with the configuration changes you need. For example, if you're using [secrets management with Vault]({{< ref "secrets-vault" >}})(![Proprietary](/images/proprietary.svg)), Halyard and Operator containers need your Vault configuration:

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: halyard-custom-config
data:
  halyard-local.yml: |
    secrets:
      vault:
        enabled: true
        url: <URL of vault server>
        path: <cluster path>
        role: <k8s role>
        authMethod: KUBERNETES
```

Then, you can mount it in the Operator deployment and make it available to the Halyard and Operator containers:

```yaml
apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: spinnaker-operator
  ...
spec:
  template:
    spec:
      containers:
      - name: spinnaker-operator
        ...
        volumeMounts:
        - mountPath: /opt/spinnaker/config/halyard.yml
          name: halconfig-volume
          subPath: halyard-local.yml
      - name: halyard
        ...
        volumeMounts:
        - mountPath: /opt/spinnaker/config/halyard-local.yml
          name: halconfig-volume
          subPath: halyard-local.yml
      volumes:
      - configMap:
          defaultMode: 420
          name: halyard-custom-config
        name: halconfig-volume
```

## Patching Runtime Resources with Kustomize

Your Kubernetes cluster may require additional sidecars or configuration
present when managing Spinnaker resources. In these situations, the Armory
Operator provides the ability to patch resources during reconciliation. These
patches are executed via an embedded Kustomize instance in the Operator, and
requires no additional installation on the user's part. You can apply Kustomize
patches at two levels of specificity:

- Spinnaker as a whole
- Individual services within Spinnaker

Additionally, you may make changes to the following resources generated by
the Operator:

- `Deployment` manifests
- `Service` manifests

For example, to ensure that a `ConfigMap` is present on all Spinnaker services,
you would add the following configuration block to your `SpinnakerService`
config:

{{< highlight yaml "linenos=table,hl_lines=5-9" >}}
apiVersion: spinnaker.armory.io/v1alpha2
kind: SpinnakerService
metadata:
  name: spinnaker
spec:
  kustomize:
    spinnaker:
      deployment:
        patchesJson6902: |
          - op: add
            path: /spec/template/spec/volumes/-
            value:
              name: custom-volume
              configMap:
                name: custom-volume
          - op: add
            path: /spec/template/spec/containers/0/volumeMounts/-
            value:
              mountPath: /opt/spinnaker/config/foo
              type: configMap
              name: custom-volume
{{< /highlight >}}

The previous configuration sample indicates how to specify patches in the
[`patchesJson6902`
format](https://kubectl.docs.kubernetes.io/references/kustomize/kustomization/patchesjson6902/),
that mounts a `ConfigMap` called `custom-volume` into the
`/opt/spinnaker/config/foo` namespace.

When you no longer need the patches, you can remove them from the Operator
config and they will be removed on next reconciliation for your cluster.

## Help resources

{{% include "armory-operator/help-resources.md" %}}
