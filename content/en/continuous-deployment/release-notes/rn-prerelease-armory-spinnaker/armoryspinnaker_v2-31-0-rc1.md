---
title: v2.31.0-rc1 Armory Release (OSS Spinnaker™ v1.31.2)
toc_hide: true
date: 2023-10-10
version: <!-- version in 00.00.00 format ex 02.23.01 for sorting, grouping -->
description: >
  Release notes for Armory Continuous Deployment v2.31.0-rc1. A beta release is not meant for installation in production environments.

---

## 2023/10/10 Release Notes

## Disclaimer

This pre-release software is to allow limited access to test or beta versions of the Armory services (“Services”) and to provide feedback and comments to Armory regarding the use of such Services. By using Services, you agree to be bound by the terms and conditions set forth herein.

Your Feedback is important and we welcome any feedback, analysis, suggestions and comments (including, but not limited to, bug reports and test results) (collectively, “Feedback”) regarding the Services. Any Feedback you provide will become the property of Armory and you agree that Armory may use or otherwise exploit all or part of your feedback or any derivative thereof in any manner without any further remuneration, compensation or credit to you. You represent and warrant that any Feedback which is provided by you hereunder is original work made solely by you and does not infringe any third party intellectual property rights.

Any Feedback provided to Armory shall be considered Armory Confidential Information and shall be covered by any confidentiality agreements between you and Armory.

You acknowledge that you are using the Services on a purely voluntary basis, as a means of assisting, and in consideration of the opportunity to assist Armory to use, implement, and understand various facets of the Services. You acknowledge and agree that nothing herein or in your voluntary submission of Feedback creates any employment relationship between you and Armory.

Armory may, in its sole discretion, at any time, terminate or discontinue all or your access to the Services. You acknowledge and agree that all such decisions by Armory are final and Armory will have no liability with respect to such decisions.

YOUR USE OF THE SERVICES IS AT YOUR OWN RISK. THE SERVICES, THE ARMORY TOOLS AND THE CONTENT ARE PROVIDED ON AN “AS IS” BASIS, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. ARMORY AND ITS LICENSORS MAKE NO REPRESENTATION, WARRANTY, OR GUARANTY AS TO THE RELIABILITY, TIMELINESS, QUALITY, SUITABILITY, TRUTH, AVAILABILITY, ACCURACY OR COMPLETENESS OF THE SERVICES, THE ARMORY TOOLS OR ANY CONTENT. ARMORY EXPRESSLY DISCLAIMS ON ITS OWN BEHALF AND ON BEHALF OF ITS EMPLOYEES, AGENTS, ATTORNEYS, CONSULTANTS, OR CONTRACTORS ANY AND ALL WARRANTIES INCLUDING, WITHOUT LIMITATION (A) THE USE OF THE SERVICES OR THE ARMORY TOOLS WILL BE TIMELY, UNINTERRUPTED OR ERROR-FREE OR OPERATE IN COMBINATION WITH ANY OTHER HARDWARE, SOFTWARE, SYSTEM OR DATA, (B) THE SERVICES AND THE ARMORY TOOLS AND/OR THEIR QUALITY WILL MEET CUSTOMER”S REQUIREMENTS OR EXPECTATIONS, (C) ANY CONTENT WILL BE ACCURATE OR RELIABLE, (D) ERRORS OR DEFECTS WILL BE CORRECTED, OR (E) THE SERVICES, THE ARMORY TOOLS OR THE SERVER(S) THAT MAKE THE SERVICES AVAILABLE ARE FREE OF VIRUSES OR OTHER HARMFUL COMPONENTS. CUSTOMER AGREES THAT ARMORY SHALL NOT BE RESPONSIBLE FOR THE AVAILABILITY OR ACTS OR OMISSIONS OF ANY THIRD PARTY, INCLUDING ANY THIRD-PARTY APPLICATION OR PRODUCT, AND ARMORY HEREBY DISCLAIMS ANY AND ALL LIABILITY IN CONNECTION WITH SUCH THIRD PARTIES.

IN NO EVENT SHALL ARMORY, ITS EMPLOYEES, AGENTS, ATTORNEYS, CONSULTANTS, OR CONTRACTORS BE LIABLE UNDER THIS AGREEMENT FOR ANY CONSEQUENTIAL, SPECIAL, LOST PROFITS, INDIRECT OR OTHER DAMAGES, INCLUDING BUT NOT LIMITED TO LOST PROFITS, LOSS OF BUSINESS, COST OF COVER WHETHER BASED IN CONTRACT, TORT (INCLUDING NEGLIGENCE), OR OTHERWISE, EVEN IF ARMORY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES AND NOTWITHSTANDING ANY FAILURE OF ESSENTIAL PURPOSE OF ANY LIMITED REMEDY. IN ANY EVENT, ARMORY, ITS EMPLOYEES’, AGENTS’, ATTORNEYS’, CONSULTANTS’ OR CONTRACTORS’ AGGREGATE LIABILITY UNDER THIS AGREEMENT FOR ANY CLAIM SHALL BE STRICTLY LIMITED TO $100.00. SOME STATES DO NOT ALLOW THE LIMITATION OR EXCLUSION OF LIABILITY FOR INCIDENTAL OR CONSEQUENTIAL DAMAGES, SO THE ABOVE LIMITATION OR EXCLUSION MAY NOT APPLY TO YOU.

You acknowledge that Armory has provided the Services in reliance upon the limitations of liability set forth herein and that the same is an essential basis of the bargain between the parties.


## Required Armory Operator version

To install, upgrade, or configure Armory 2.31.0-rc1, use Armory Operator 1.70 or later.

## Security

Armory scans the codebase as we develop and release software. Contact your Armory account representative for information about CVE scans for this release.

## Breaking changes
<!-- Copy/paste from the previous version if there are recent ones. We can drop breaking changes after 3 minor versions. Add new ones from OSS and Armory. -->

> Breaking changes are kept in this list for 3 minor versions from when the change is introduced. For example, a breaking change introduced in 2.21.0 appears in the list up to and including the 2.24.x releases. It would not appear on 2.25.x release notes.

## Known issues
<!-- Copy/paste known issues from the previous version if they're not fixed. Add new ones from OSS and Armory. If there aren't any issues, state that so readers don't think we forgot to fill out this section. -->

## Highlighted updates

<!--
Each item category (such as UI) under here should be an h3 (###). List the following info that service owners should be able to provide:
- Major changes or new features we want to call out for Armory and OSS. Changes should be grouped under end user understandable sections. For example, instead of Deck, use UI. Instead of Fiat, use Permissions.
- Fixes to any known issues from previous versions that we have in release notes. These can all be grouped under a Fixed issues H3.
-->




###  Spinnaker Community Contributions

There have also been numerous enhancements, fixes, and features across all of Spinnaker's other services. See the
[Spinnaker v1.31.2](https://www.spinnaker.io/changelogs/1.31.2-changelog/) changelog for details.

## Detailed updates

### Bill Of Materials (BOM)

Here's the BOM for this version.
<details><summary>Expand</summary>
<pre class="highlight">
<code>artifactSources:
  dockerRegistry: docker.io/armory
dependencies:
  redis:
    commit: null
    version: 2:2.8.4-2
services:
  clouddriver:
    commit: ea07a68277aa69b0b102f0f8544d1dbec8272efa
    version: 2.31.0-rc1
  deck:
    commit: 7622cd858f68342b11262cebffc60b6b04f6a9b0
    version: 2.31.0-rc1
  dinghy:
    commit: 5d44db0f3b4815075a90ef7121df6b830a39e6d5
    version: 2.31.0-rc1
  echo:
    commit: 97578efdbccaa5ffe64586166382d9d667bad93f
    version: 2.31.0-rc1
  fiat:
    commit: 218510ad92451ccfcaf345332fa09087e0229341
    version: 2.31.0-rc1
  front50:
    commit: 07267503a90b987c1c6dbdeee88160d7a1b6c7f2
    version: 2.31.0-rc1
  gate:
    commit: 7b4de74187812e3e12f783661de79b223d9f53b4
    version: 2.31.0-rc1
  igor:
    commit: 3c9dd843c3eddbfaa529f054b2df73de938391ca
    version: 2.31.0-rc1
  kayenta:
    commit: cb7a0d94e995c51486cc214cec45b1f983817c0d
    version: 2.31.0-rc1
  monitoring-daemon:
    commit: null
    version: 2.26.0
  monitoring-third-party:
    commit: null
    version: 2.26.0
  orca:
    commit: 238fc61ed93dd33702377f756455b44fff5acb5d
    version: 2.31.0-rc1
  rosco:
    commit: ca913887ada366fcb17987672a6315c6c65ca634
    version: 2.31.0-rc1
  terraformer:
    commit: 30d6e5f1f249df9d543f4e1e4738c1af59a53e8e
    version: 2.31.0-rc1
timestamp: "2023-10-10 08:50:14"
version: 2.31.0-rc1
</code>
</pre>
</details>

### Armory


#### Armory Fiat - 2.30.0...2.31.0-rc1

  - fix(okhttp): Decrypt properties before creating client. (#501)
  - chore(cd): update base service version to fiat:2023.07.21.15.45.35.release-1.30.x (#496)
  - chore(cd): update armory-commons version to 3.13.5 (#478)
  - chore(cd): update armory-commons version to 3.13.3 (#475)
  - chore(cd): update armory-commons version to 3.13.2 (#471)
  - chore(cd): update base service version to fiat:2023.04.05.11.36.40.release-1.30.x (#470)
  - chore(cd): update armory-commons version to 3.13.1 (#456)
  - chore(cd): update base service version to fiat:2023.02.20.19.50.58.master (#437)
  - chore(armory-commons): upgrading armory-commons to 3.14.0-rc.3 (#497)
  - chore(cd): update armory-commons version to 3.14.2 (#500)
  - fix(okhttp): Decrypt properties before creating client. (#501) (#504)
  - chore(ci): removed aquasec scan action (#523) (#525)

#### Dinghy™ - 2.30.0...2.31.0-rc1

  - chore(ci): removed aquasec scan action (#489) (#491)
  - chore(ci): removing aquasec scans for any push (#497) (#498)

#### Armory Gate - 2.30.0...2.31.0-rc1

  - chore(cd): update armory-commons version to 3.13.3 (#559)
  - fix(tests): Fix JUnit tests (#558)
  - chore(cd): update base service version to gate:2023.04.07.01.27.28.release-1.30.x (#553)
  - chore(cd): update armory-commons version to 3.13.2 (#554)
  - chore(cd): update armory-commons version to 3.13.1 (#537)
  - revert(header): update plugins.json with newest header version (#484)
  - chore(cd): update base service version to gate:2023.04.17.18.59.00.master (#557)
  - chore(cd): update base service version to gate:2023.05.02.16.41.37.master (#560)
  - chore(cd): update base service version to gate:2023.05.02.16.49.52.master (#561)
  - chore(cd): update base service version to gate:2023.05.12.14.58.29.master (#562)
  - chore(cd): update base service version to gate:2023.05.18.17.05.02.master (#564)
  - chore(cd): update base service version to gate:2023.05.25.21.38.35.master (#565)
  - chore(cd): update base service version to gate:2023.06.02.20.01.30.master (#566)
  - chore(cd): update base service version to gate:2023.06.05.20.11.44.master (#567)
  - chore(cd): update base service version to gate:2023.06.12.23.37.52.master (#568)
  - chore(cd): update base service version to gate:2023.06.13.05.17.05.master (#569)
  - chore(cd): update base service version to gate:2023.06.16.09.48.18.master (#570)
  - chore(cd): update base service version to gate:2023.06.17.10.05.03.master (#571)
  - chore(cd): update base service version to gate:2023.06.26.17.12.12.master (#572)
  - chore(cd): update base service version to gate:2023.06.28.20.06.44.master (#573)
  - chore(armory-commons): upgrading armory-commons to 3.14.0-rc.3 (#583)
  - chore(cd): update armory-commons version to 3.14.2 (#586)
  - chore(cd): update base service version to gate:2023.08.28.17.15.40.release-1.31.x (#600)
  - chore(cd): update base service version to gate:2023.08.29.05.01.02.release-1.31.x (#604)
  - fix: esapi CVE scan report (#602) (#605)
  - chore(cd): update base service version to gate:2023.09.01.15.43.46.release-1.31.x (#607)
  - chore(ci): removed aquasec scan action (#616) (#621)

#### Armory Echo - 2.30.0...2.31.0-rc1

  - chore(cd): update armory-commons version to 3.13.5 (#583)
  - chore(cd): update armory-commons version to 3.13.4 (#580)
  - chore(cd): update armory-commons version to 3.13.3 (#578)
  - chore(cd): update armory-commons version to 3.13.2 (#575)
  - chore(cd): update base service version to echo:2023.04.07.01.30.15.release-1.30.x (#573)
  - chore(cd): update base service version to echo:2023.04.05.11.38.02.release-1.30.x (#572)
  - chore(cd): update armory-commons version to 3.13.1 (#558)
  - chore(cd): update base service version to echo:2023.02.20.21.09.15.master (#539)
  - chore(cd): update armory-commons version to 3.14.2 (#601)
  - chore(ci): removed aquasec scan action (#618) (#621)
  - chore(cd): update base service version to echo:2023.08.29.05.00.24.release-1.31.x (#612)

#### Armory Deck - 2.30.0...2.31.0-rc1

  - chore(cd): update base deck version to 2023.0.0-20230621174859.release-1.30.x (#1335)
  - chore(cd): update base deck version to 2023.0.0-20230321144223.release-1.30.x (#1331)
  - chore(cd): update base deck version to 2023.0.0-20230220132814.master (#1300)
  - chore(alpine): Upgrade alpine version (#1302)
  - chore(cd): update base deck version to 2023.0.0-20230308202716.master (#1305)
  - chore(cd): update base deck version to 2023.0.0-20230309231023.master (#1306)
  - chore(cd): update base deck version to 2023.0.0-20230310120132.master (#1307)
  - chore(cd): update base deck version to 2023.0.0-20230315120430.master (#1308)
  - chore(cd): update base deck version to 2023.0.0-20230321144223.master (#1309)
  - chore(cd): update base deck version to 2023.0.0-20230329194405.master (#1310)
  - chore(cd): update base deck version to 2023.0.0-20230330162636.master (#1311)
  - chore(cd): update base deck version to 2023.0.0-20230331215046.master (#1312)
  - chore(cd): update base deck version to 2023.0.0-20230331223352.master (#1313)
  - chore(cd): update base deck version to 2023.0.0-20230331235900.master (#1317)
  - chore(cd): update base deck version to 2023.0.0-20230401002322.master (#1318)
  - chore(build): only run security scans on PR merge (#1319)
  - chore(cd): update base deck version to 2023.0.0-20230401030506.master (#1320)
  - chore(cd): update base deck version to 2023.0.0-20230402044748.master (#1322)
  - chore(cd): update base deck version to 2023.0.0-20230402051752.master (#1323)
  - chore(cd): update base deck version to 2023.0.0-20230402053723.master (#1324)
  - chore(cd): update base deck version to 2023.0.0-20230403112432.master (#1325)
  - chore(ci): removed aquasec scan action (#1340) (#1344)

#### Armory Kayenta - 2.30.0...2.31.0-rc1

  - chore(cd): update armory-commons version to 3.13.5 (#439)
  - fix: Remove whitespace when defining spring properties (#437) (#438)
  - fix(config): add missing exclude spring config (#435) (#436)
  - fix: Update path of main class. (#432)
  - chore(refactoring): refactored setting default system properties (#429)
  - chore(cd): update armory-commons version to 3.13.3 (#428)
  - chore(cd): update base service version to kayenta:2023.04.13.23.42.23.release-1.30.x (#427)
  - chore(cd): update armory-commons version to 3.13.2 (#424)
  - chore(cd): update base service version to kayenta:2023.01.24.16.10.35.master (#387)
  - fix: Update path of main class. (#432) (#433)
  - fix(config): add missing exclude spring config (#435)
  - fix: Remove whitespace when defining spring properties (#437)
  - chore(cd): update armory-commons version to 3.14.2 (#456)
  - chore(ci): removed aquasec scan action (#469) (#470)

#### Terraformer™ - 2.30.0...2.31.0-rc1

  - chore(alpine): Update alpine version (#497)
  - chore(ci): removing aquasec scans on push (#517) (#518)

#### Armory Front50 - 2.30.0...2.31.0-rc1

  - chore(cd): update base service version to front50:2023.05.22.19.11.48.release-1.30.x (#548)
  - chore(cd): update armory-commons version to 3.13.3 (#538)
  - chore(cd): update base service version to front50:2023.04.27.18.45.08.release-1.30.x (#541)
  - chore(cd): update armory-commons version to 3.13.2 (#533)
  - chore(cd): update armory-commons version to 3.13.1 (#514)
  - chore(cd): update base service version to front50:2023.04.07.01.28.32.release-1.30.x (#532)
  - chore(dockerfile): upgrade to latest alpine image (#434)
  - chore(cd): update base service version to front50:2023.04.05.11.05.16.master (#529)
  - chore(cd): update base service version to front50:2023.04.21.14.37.41.master (#540)
  - chore(cd): update base service version to front50:2023.05.02.05.06.08.master (#542)
  - chore(armory-commons): upgrading armory-commons to 3.14.0-rc.3 (#564)
  - chore(cd): update base service version to front50:2023.07.18.21.40.31.master (#563)
  - chore(cd): update armory-commons version to 3.14.2 (#567)
  - chore(cd): update base service version to front50:2023.08.28.17.17.25.release-1.31.x (#580)
  - chore(cd): update base service version to front50:2023.08.29.04.59.48.release-1.31.x (#581)
  - chore(cd): update base service version to front50:2023.09.05.18.25.32.release-1.31.x (#584)
  - chore(ci): removed aquasec scan action (#590) (#593)

#### Armory Igor - 2.30.0...2.31.0-rc1

  - chore(cd): update armory-commons version to 3.13.3 (#452)
  - chore(cd): update armory-commons version to 3.13.2 (#449)
  - chore(cd): update base service version to igor:2023.04.07.01.27.38.release-1.30.x (#448)
  - chore(cd): update armory-commons version to 3.13.1 (#431)
  - chore(cd): update base service version to igor:2022.09.14.15.59.58.master (#368)

#### Armory Orca - 2.30.0...2.31.0-rc1

  - chore(cd): update base orca version to 2023.06.29.14.44.25.release-1.30.x (#658)
  - chore(cd): update base orca version to 2023.06.20.15.55.26.release-1.30.x (#656)
  - chore(cd): update base orca version to 2023.05.18.14.27.05.release-1.30.x (#644)
  - chore(cd): update armory-commons version to 3.13.5 (#642)
  - chore(cd): update armory-commons version to 3.13.4 (#637)
  - chore(cd): update armory-commons version to 3.13.3 (#635)
  - chore(build): Backport missing build changes (#634)
  - chore(cd): update armory-commons version to 3.13.2 (#630)
  - chore(cd): update base orca version to 2023.04.07.01.52.33.release-1.30.x (#629)
  - chore(cd): update armory-commons version to 3.13.1 (#613)
  - chore(cd): update base orca version to 2022.04.01.22.15.58.master (#459)

#### Armory Clouddriver - 2.30.0...2.31.0-rc1

  - chore(cd): update base service version to clouddriver:2023.05.30.19.45.40.release-1.30.x (#882)
  - chore(cd): update armory-commons version to 3.13.5 (#874)
  - chore(cd): update armory-commons version to 3.13.4 (#869)
  - chore(cd): update armory-commons version to 3.13.3 (#867)
  - chore(cd): update armory-commons version to 3.13.2 (#861)
  - chore(cd): update base service version to clouddriver:2023.04.07.02.16.05.release-1.30.x (#860)
  - chore(cd): update base service version to clouddriver:2023.04.06.10.03.44.release-1.30.x (#859)
  - chore(cd): update base service version to clouddriver:2023.04.05.14.02.06.release-1.30.x (#856)
  - chore(cd): update base service version to clouddriver:2023.03.24.23.48.26.release-1.30.x (#839)
  - chore(cd): update armory-commons version to 3.13.1 (#837)
  - chore(cd): update base service version to clouddriver:2023.03.18.00.04.47.master (#818)
  - chore(cd): update base service version to clouddriver:2023.03.21.00.31.33.master (#819)
  - chore(cd): update base service version to clouddriver:2023.03.21.19.49.36.master (#820)
  - chore(cd): update base service version to clouddriver:2023.03.22.20.00.03.master (#824)
  - chore(cd): update base service version to clouddriver:2023.03.23.21.01.03.master (#827)
  - chore(cd): update base service version to clouddriver:2023.03.24.23.48.26.master (#828)
  - chore(cd): update base service version to clouddriver:2023.03.29.20.10.21.master (#834)
  - chore(cd): update base service version to clouddriver:2023.03.30.15.20.14.master (#835)
  - chore(cd): update base service version to clouddriver:2023.03.30.16.52.08.master (#838)
  - chore(cd): update base service version to clouddriver:2023.03.31.19.56.29.master (#840)
  - chore(cd): update base service version to clouddriver:2023.03.31.22.03.23.master (#841)
  - chore(cd): update base service version to clouddriver:2023.03.31.22.50.54.master (#842)
  - chore(cd): update base service version to clouddriver:2023.04.01.00.13.01.master (#843)
  - chore(cd): update base service version to clouddriver:2023.04.01.03.32.05.master (#845)
  - chore(cd): update base service version to clouddriver:2023.04.01.04.39.47.master (#846)
  - chore(cd): update base service version to clouddriver:2023.04.01.05.26.14.master (#847)
  - chore(cd): update base service version to clouddriver:2023.04.01.06.46.40.master (#848)
  - chore(cd): update base service version to clouddriver:2023.04.02.04.27.18.master (#849)
  - chore(cd): update base service version to clouddriver:2023.04.02.05.24.21.master (#850)
  - chore(cd): update base service version to clouddriver:2023.04.02.06.10.44.master (#851)
  - chore(cd): update base service version to clouddriver:2023.04.03.15.54.26.master (#852)
  - chore(cd): update base service version to clouddriver:2023.04.03.17.05.33.master (#853)
  - Bumped aws-cli to 1.22 for FIPS compliance (#854)
  - chore(cd): update base service version to clouddriver:2023.04.05.11.43.53.master (#855)
  - chore(cd): update base service version to clouddriver:2023.04.05.21.36.10.master (#857)
  - chore(cd): update base service version to clouddriver:2023.04.17.19.36.00.master (#865)
  - chore(cd): update base service version to clouddriver:2023.05.02.05.46.22.master (#871)
  - chore(cd): update base service version to clouddriver:2023.05.04.00.42.22.master (#872)
  - chore(cd): update base service version to clouddriver:2023.05.11.19.04.48.master (#873)
  - chore(cd): update base service version to clouddriver:2023.05.18.17.41.51.master (#875)
  - chore(cd): update base service version to clouddriver:2023.05.19.23.07.09.master (#876)
  - chore(cd): update base service version to clouddriver:2023.05.25.22.18.08.master (#877)
  - chore(cd): update base service version to clouddriver:2023.05.30.17.49.03.master (#879)
  - chore(cd): update base service version to clouddriver:2023.06.02.19.20.42.master (#884)
  - chore(cd): update base service version to clouddriver:2023.06.05.20.51.02.master (#885)
  - chore(cd): update armory-commons version to 3.14.2 (#911)
  - chore(cd): update base service version to clouddriver:2023.07.21.18.25.26.release-1.31.x (#915)
  - fix: AWS CLI pip installation (#918) (#924)
  - chore(cd): update base service version to clouddriver:2023.08.28.14.14.40.release-1.31.x (#939)
  - chore(cd): update base service version to clouddriver:2023.08.28.17.52.39.release-1.31.x (#941)
  - chore(cd): update base service version to clouddriver:2023.08.29.05.45.59.release-1.31.x (#942)
  - chore(cd): update base service version to clouddriver:2023.09.08.18.30.47.release-1.31.x (#968)
  - chore(cd): update base service version to clouddriver:2023.09.20.19.42.06.release-1.31.x (#981)
  - chore(ci): removed aquasec scan action (#971) (#982)
  - fix: CVE-2023-37920 (#977) (#993)

#### Armory Rosco - 2.30.0...2.31.0-rc1

  - chore(cd): update armory-commons version to 3.13.3 (#528)
  - chore(cd): update base service version to rosco:2023.04.05.11.40.04.release-1.30.x (#523)
  - chore(cd): update armory-commons version to 3.13.1 (#508)
  - feat(dockerfile): add Kustomize 4 to Dockerfiles (#434)
  - fix(rosco): added missing rosco-core dependency and upgrading embedded redis for tests (#456)
  - chore(packer): copied templates and config from oss (#457)
  - chore(cd): update base service version to rosco:2022.11.10.16.54.39.master (#458)
  - chore(cd): update base service version to rosco:2022.11.15.19.33.07.master (#459)
  - chore(cd): update base service version to rosco:2022.11.16.17.50.30.master (#460)
  - chore(cd): update base service version to rosco:2022.11.17.15.34.54.master (#461)
  - chore(cd): update base service version to rosco:2022.11.18.18.20.19.master (#462)
  - chore(cd): update base service version to rosco:2022.11.19.01.16.08.master (#463)
  - chore(cd): update base service version to rosco:2022.11.19.16.30.34.master (#464)
  - chore(cd): update base service version to rosco:2022.11.22.14.31.01.master (#466)
  - chore(azure): copying config from oss, upgrading centos (#465)
  - chore(cd): update base service version to rosco:2022.11.24.15.56.54.master (#469)
  - chore(cd): update base service version to rosco:2022.12.08.14.30.19.master (#472)
  - chore(cd): update base service version to rosco:2022.12.08.20.50.39.master (#473)
  - chore(cd): update base service version to rosco:2022.12.09.00.48.23.master (#476)
  - chore(cd): update base service version to rosco:2022.12.09.02.57.42.master (#477)
  - chore(cd): update base service version to rosco:2022.12.09.06.01.36.master (#478)
  - chore(cd): update base service version to rosco:2022.12.09.17.27.05.master (#479)
  - fix(build): Add javax.validation dependency (#480)
  - chore(cd): update base service version to rosco:2022.12.15.16.52.34.master (#481)
  - chore(cd): update base service version to rosco:2022.12.22.04.48.59.master (#482)
  - chore(cd): update base service version to rosco:2023.01.12.21.47.32.master (#485)
  - chore(cd): update base service version to rosco:2023.01.23.17.14.17.master (#487)
  - chore(cd): update base service version to rosco:2023.01.27.00.40.58.master (#488)
  - chore(cd): update base service version to rosco:2023.01.30.16.28.07.master (#489)
  - chore(cd): update base service version to rosco:2023.02.08.19.46.54.master (#490)
  - chore(cd): update base service version to rosco:2023.02.08.22.19.58.master (#491)
  - chore(cd): update base service version to rosco:2023.02.08.23.30.28.master (#492)
  - chore(cd): update base service version to rosco:2023.02.09.00.57.01.master (#493)
  - chore(cd): update base service version to rosco:2023.02.09.06.34.37.master (#494)
  - chore(cd): update base service version to rosco:2023.02.16.16.48.52.master (#495)
  - chore(cd): update base service version to rosco:2023.02.20.19.50.47.master (#496)
  - chore(cd): update armory-commons version to 3.9.5 (#505)
  - chore(armory-commons): upgrading armory-commons to 3.14.0-rc.3 (#549)
  - chore(cd): update armory-commons version to 3.14.2 (#552)
  - chore(ci): removed aquasec scan action (#565) (#567)
  - chore(cd): update base service version to rosco:2023.08.28.17.15.52.release-1.31.x (#562)


### Spinnaker


#### Spinnaker Fiat - 1.31.2

  - chore(dependencies): Autobump korkVersion (#1050)
  - chore(dependencies): Autobump korkVersion (#1033)
  - fix(logs): Redacted secret data in logs. (#1029)
  - chore(dependencies): Autobump korkVersion (#1028)
  - fix(tests): Introduce junit5 vintage engine for running junit4 test cases over junit5 in fiat (#1025)
  - chore(dependencies): Autobump korkVersion (#1023)
  - chore(dependencies): Autobump korkVersion (#1022)

#### Spinnaker Gate - 1.31.2

  - chore(dependencies): Autobump korkVersion (#1649)
  - chore(dependencies): Autobump fiatVersion (#1630)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1634)
  - chore(dependencies): Autobump fiatVersion (#1635)
  - chore(gha): update to docker/login-action@v2 to stay up to date (#1636)
  - chore(dependencies): Autobump korkVersion (#1637)
  - chore(dependencies): Autobump fiatVersion (#1638)
  - feat(gha): configure dependabot to keep github actions up to date (#1639)
  - chore(deps): bump google-github-actions/auth from 0 to 1 (#1641)
  - chore(deps): bump actions/checkout from 2 to 3 (#1642)
  - chore(deps): bump google-github-actions/upload-cloud-storage from 0 to 1 (#1644)
  - chore(deps): bump docker/build-push-action from 3 to 4 (#1640)
  - chore(deps): bump actions/setup-java from 2 to 3 (#1643)
  - chore(gha): replace action for creating github releases (#1645)
  - chore(gha): replace deprecated set-output commands with environment files (#1646)
  - chore(dependencies): Autobump korkVersion (#1647)
  - chore(dependencies): Autobump korkVersion (#1648)
  - chore(dependencies): Autobump korkVersion (#1652)
  - fix(web/test): move GateConfigAuthenticatedRequestFilterTest out of the com.netflix.spinnaker.gate.config package (#1655)
  - chore(dependencies): Autobump korkVersion (#1654)
  - fix(web/test): remove race in FunctionalSpec (#1657)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1658)
  - chore(dependencies): Autobump korkVersion (#1659)
  - chore(dependencies): Autobump korkVersion (#1661)
  - chore(dependencies): Autobump fiatVersion (#1662)
  - chore(dependencies): Autobump korkVersion (#1695)
  - chore(dependencies): Autobump fiatVersion (#1697)
  - fix(cachingFilter: Allow disabling the content caching filter (#1699) (#1701)

#### Spinnaker Echo - 1.31.2

  - chore(dependencies): Autobump korkVersion (#1288)
  - chore(dependencies): Autobump fiatVersion (#1268)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1272)
  - chore(dependencies): Autobump fiatVersion (#1273)
  - chore(gha): update to docker/login-action@v2 to stay up to date (#1274)
  - chore(dependencies): Autobump korkVersion (#1275)
  - chore(dependencies): Autobump fiatVersion (#1276)
  - feat(gha): configure dependabot to keep github actions up to date (#1277)
  - chore(deps): bump docker/build-push-action from 2 to 4 (#1279)
  - chore(deps): bump google-github-actions/auth from 0 to 1 (#1280)
  - chore(deps): bump google-github-actions/upload-cloud-storage from 0 to 1 (#1278)
  - chore(deps): bump actions/setup-java from 2 to 3 (#1282)
  - chore(deps): bump actions/checkout from 2 to 3 (#1281)
  - chore(gha): replace action for creating github releases (#1283)
  - chore(gha): replace deprecated set-output commands with environment files (#1284)
  - chore(dependencies): Autobump korkVersion (#1285)
  - chore(dependencies): Autobump korkVersion (#1286)
  - chore(dependencies): Autobump korkVersion (#1287)
  - chore(dependencies): Autobump korkVersion (#1291)
  - feat(pipelinetriggers): only cache enabled pipelines with enabled triggers of specific types (#1292)
  - chore(dependencies): Autobump korkVersion (#1293)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1296)
  - chore(dependencies): Autobump korkVersion (#1297)
  - chore(dependencies): Autobump korkVersion (#1298)
  - chore(dependencies): Autobump fiatVersion (#1299)
  - fix(gha): Fix github status log and add tests (#1316) (#1318)
  - chore(dependencies): Autobump korkVersion (#1333)
  - chore(dependencies): Autobump fiatVersion (#1334)

#### Spinnaker Deck - 1.31.2

  - Publish packages to NPM (#9955)
  - chore(dependencies): Autobump spinnakerGradleVersion (#9957)
  - chore(gha): update to docker/login-action@v2 to stay up to date (#9958)
  - chore(gha): replace deprecated set-output commands (#9952)
  - feat(gha): configure dependabot to keep github actions up to date (#9959)
  - chore(deps): bump actions/github-script from 0.9.0 to 6.4.0 (#9962)
  - chore(deps): bump google-github-actions/upload-cloud-storage from 0 to 1 (#9966)
  - chore(deps): bump peter-evans/create-pull-request from 3 to 4 (#9964)
  - chore(deps): bump docker/build-push-action from 3 to 4 (#9963)
  - chore(deps): bump google-github-actions/auth from 0 to 1 (#9965)
  - chore(gha): replace action for creating github releases (#9961)
  - chore(deps): bump actions/setup-node from 1 to 3 (#9967)
  - chore(deps): bump actions/cache from 1 to 3 (#9970)
  - chore(deps): bump actions/setup-java from 2 to 3 (#9969)
  - chore(deps): bump actions/checkout from 2 to 3 (#9968)
  - fix: UI crashes when running pipeline(s) with many stages. (#9960)

#### Spinnaker Kayenta - 1.31.2

  - fix(signalfx): Fixed metric type missing due to duplicated field from parent class (#957) (#958)
  - chore(dependencies): Autobump orcaVersion (#956)
  - chore(dependencies): Autobump orcaVersion (#941)
  - feat: SPLAT-569: Add SQL data source for account credentials and account configurations persistence. (#938)
  - chore(dependencies): Autobump orcaVersion (#932)
  - chore(dependencies): Autobump orcaVersion (#931)
  - chore(dependencies): remove dependency on groovy-all in kayenta (#930)
  - chore(cleanup): Doing refactoring of Kayenta to cleanup codebase (#926)
  - chore(dependency): unpinning the version of io.rest-assured (#929)

#### Spinnaker Front50 - 1.31.2

  - fix(validator): Fix NPE when traffic management is not defined in a deployment manifest (#1253) (#1254)
  - chore(dependencies): Autobump fiatVersion (#1248)
  - chore(dependencies): don't create an autobump PR for halyard on a front50 release branch (#1115) (#1247)
  - chore(dependencies): Autobump korkVersion (#1246)
  - chore(dependencies): Autobump fiatVersion (#1225)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1229)
  - chore(dependencies): Autobump fiatVersion (#1230)
  - chore(gha): update to docker/login-action@v2 to stay up to date (#1231)
  - chore(dependencies): Autobump korkVersion (#1232)
  - chore(dependencies): Autobump fiatVersion (#1233)
  - feat(gha): configure dependabot to keep github actions up to date (#1234)
  - chore(deps): bump actions/checkout from 2 to 3 (#1235)
  - chore(deps): bump google-github-actions/upload-cloud-storage from 0 to 1 (#1238)
  - chore(deps): bump peter-evans/repository-dispatch from 1 to 2 (#1236)
  - chore(deps): bump docker/build-push-action from 3 to 4 (#1237)
  - chore(deps): bump actions/setup-java from 2 to 3 (#1239)
  - chore(gha): replace action for creating github releases (#1240)
  - chore(deps): bump google-github-actions/auth from 0 to 1 (#1242)
  - chore(dependencies): Autobump korkVersion (#1243)
  - chore(dependencies): Autobump korkVersion (#1244)
  - chore(gha): replace deprecated set-output commands with environment files (#1241)
  - chore(dependencies): Autobump korkVersion (#1245)
  - chore(dependencies): Autobump korkVersion (#1250)
  - feat(core + sql): Optimize cache refresh (#1249)
  - feat(pipelines): add new GET /pipelines/triggeredBy/{id:.+}/{status} endpoint (#1251)
  - feat(web): add optional query params to the GET /pipelines endpoint (#1252)
  - fix(validator): Fix NPE when traffic management is not defined in a deployment manifest (#1253)
  - chore(dependencies): Autobump korkVersion (#1255)
  - perf(sql): add index on last_modified_at (#1256)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1258)
  - refactor(deprecation): remove deprecated gradle constructs/features from front50 in order to upgrade gradle 7 (#1257)
  - fix(migrations): do not migrate redblack pipelines without stages (#1259)
  - chore(dependencies): Autobump korkVersion (#1262)
  - chore(dependencies): Autobump korkVersion (#1263)
  - chore(dependencies): Autobump fiatVersion (#1264)
  - fix(web): check trigger.getType() for null before invoking equals method (#1277) (#1278)
  - fix(core): tolerate items with null ids (#1276) (#1280)
  - fix(core): skip existing items with null ids in StorageServiceSupport.fetchAllItemsOptimized (#1279) (#1281)
  - chore(dependencies): Autobump korkVersion (#1299)
  - chore(dependencies): Autobump fiatVersion (#1300)
  - fix(dependency): fix dependency version leak of google-api-services-storage from kork in front50-web (#1302) (#1384)

#### Spinnaker Igor - 1.31.2

  - chore(dependencies): Autobump korkVersion (#1120)
  - chore(dependencies): Autobump fiatVersion (#1099)
  - chore(dependencies): Autobump korkVersion (#1098)
  - chore(dependencies): Autobump korkVersion (#1097)
  - fix(travis): Don't panic if log fetching fails (#1089)
  - chore(dependencies): Autobump korkVersion (#1088)
  - chore(dependencies): Autobump korkVersion (#1087)
  - chore(dependencies): remove dependency on groovy-all with required groovy package (#1086)
  - chore(dependencies): Autobump korkVersion (#1085)
  - chore(dependencies): Autobump korkVersion (#1084)
  - chore(dependencies): Autobump korkVersion (#1083)
  - chore(dependencies): Autobump korkVersion (#1082)
  - chore(dependencies): Autobump korkVersion (#1081)
  - chore(dependencies): Autobump korkVersion (#1080)
  - fix(travis): Redis TTL is given in seconds, not minutes (#1077)
  - chore(dependencies): Autobump korkVersion (#1079)
  - chore(dependencies): Autobump korkVersion (#1078)
  - fix(travis): Enable legacy log fetching (#1075)
  - feat(travis): Add redis TTL for queue keys (#1076)
  - chore(dependencies): Autobump korkVersion (#1074)
  - fix(gitlabci): Fixed JSON parsing exceptions for unknown GitlabCI pipeline statuses (#1073)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1072)
  - chore(dependencies): Autobump korkVersion (#1071)
  - chore(dependencies): remove dependency on groovy-all where straightforward (#1070)
  - chore(dependencies): Autobump korkVersion (#1069)
  - chore(dependencies): Autobump korkVersion (#1068)
  - chore(dependencies): Autobump korkVersion (#1067)
  - chore(dependencies): Autobump korkVersion (#1066)
  - refactor(web): Clean up redundant spring property in gradle file (#1065)
  - chore(dependencies): Autobump korkVersion (#1059)
  - chore(dependencies): Autobump korkVersion (#1058)
  - chore(dependencies): Autobump korkVersion (#1057)
  - chore(dependencies): Autobump spinnakerGradleVersion (#1055)
  - fix(monitor): rename parameter to let spring know what bean inject (#1053)
  - chore(dependencies): Autobump korkVersion (#1046)
  - chore(dependencies): Autobump korkVersion (#1045)
  - chore(dependencies): Autobump korkVersion (#1044)
  - chore(dependencies): Autobump korkVersion (#1043)
  - chore(dependencies): Autobump fiatVersion (#1042)

#### Spinnaker Orca - 1.31.2

  - fix(queue): fix ability to cancel a zombied execution (#4473) (#4478)
  - fix(queue): Manual Judgment propagation (#4474)
  - fix(deployment): fixed missing namespace while fetching manifest details from clouddriver (#4453) (#4457)
  - chore(dependencies): Autobump korkVersion (#4444) (#4446)
  - chore(dependencies): Autobump korkVersion (#4444)
  - chore(dependencies): Autobump fiatVersion (#4417)
  - Fix/blue green deploy (#4414)
  - chore(dependencies): Autobump korkVersion (#4413)
  - feat(igor): Default the feature flag which sends the job name as query parameter to on (#4412)
  - chore(dependencies): Autobump korkVersion (#4411)
  - Revert "feat(k8s): Add support of Deployment kind for Blue/Green deployments." (#4407)
  - fix(artifacts): Stop copying expectedArtifactIds to child pipelines (#4404)
  - fix(artifacts): Be more lenient when filtering expected artifacts (#4397)
  - fix(waiting-executions) : Waiting executions doesn't follow FIFO (#4356)
  - chore(dependencies): Autobump korkVersion (#4399)
  - chore(dependencies): Autobump korkVersion (#4398)
  - chore(dependencies): Autobump korkVersion (#4394)
  - chore(dependencies): Autobump korkVersion (#4393)
  - chore(dependencies): Autobump korkVersion (#4392)
  - chore(dependencies): Autobump korkVersion (#4391)
  - chore(dependencies): Autobump korkVersion (#4390)
  - fix(timeout): Added feature flag for rollback timeout ui input. (#4383)
  - feat(config): allow configuration of writeable clouddriver endpoints by account and/or cloudProvider (#4287)
  - chore(dependencies): Autobump korkVersion (#4381)
  - chore(dependencies): Autobump korkVersion (#4380)
  - chore(dependencies): Autobump korkVersion (#4378)
  - chore(web): clean up for spring property setup (#4377)
  - chore(dependencies): Autobump korkVersion (#4376)
  - fix(dependency): Issue with keiko-redis-spring module while upgrading the spring boot 2.5.x (#4375)
  - feat(tasks): Capture task output data from clouddriver (#4374)
  - fix(stageExecution): Extend MJ auth propagate logic for exhaustive cases (#4368)
  - chore(dependencies): Autobump spinnakerGradleVersion (#4371)
  - Fix orca bakery (#4370)
  - chore(front50): Make Monitor Pipeline Task timeout overridable (#4347)
  - feat(bakery): add tasks.monitor-bake.timeout-millis configuration property for MonitorBakeTask timeout (#4367)
  - chore(dependencies): Autobump korkVersion (#4365)
  - chore(dependencies): remove dependency on groovy-all where straightforward (#4364)
  - chore(dependencies): Autobump korkVersion (#4363)
  - chore(dependencies): Autobump korkVersion (#4362)
  - chore(dependencies): Autobump korkVersion (#4361)
  - chore(dependencies): Autobump korkVersion (#4360)
  - refactor(web): Clean up redundant spring property in gradle file (#4359)
  - feat(k8s): Add support of Deployment kind for Blue/Green deployments. (#4355)
  - feat(AWS): Get the rollback timeout value from stage data. (#4353)
  - chore(dependencies): Autobump korkVersion (#4352)
  - feat(Azure): Update createBakeTask for managed and custom images. (#4336)
  - chore(dependencies): Autobump korkVersion (#4343)
  - chore(dependencies): Autobump korkVersion (#4342)
  - fix(tasks): Fix MonitorKayentaCanaryTask on results data map (#4312)
  - chore(dependencies): Autobump spinnakerGradleVersion (#4337)
  - feat(kubernetes): Introduce blue/green traffic management strategy (#4332)
  - feat(bakery): Clean up cached data created by Rosco. (#4323)
  - fix(orca): display task exception messages (#4259)
  - feat(kubernetes events in orca): Exposes kubernetes events in orca for enhanced logging (#4301)
  - fix(config): add back public visibility for ClouddriverRetrofitBuilder class (#4331)
  - feat(bakery): add includeCRDs in Helm Bake request (#4324)
  - fix(artifacts): Expected Artifacts should be trigger specific (#4322)
  - fix(config): restore prior visibility of methods on CloudDriverConfigurationProperties class (#4317)
  - chore(dependencies): Autobump korkVersion (#4313)
  - feat(cloudrun): Adding cloudrun provider in orca. (#4311)
  - chore(kubernetes): stop specifying the version of io.kubernetes:client-java (#4310)
  - feat(cloudrun): Adding cloudrun provider in orca. (#4279)
  - fix(stageExecution): In evaluable variable stage restart scenario variables are not cleaned properly (#16) (#4307)
  - chore(dependencies): Autobump korkVersion (#4308)
  - chore(dependencies): Autobump korkVersion (#4304)
  - chore(dependencies): Autobump korkVersion (#4302)
  - chore(dependencies): Autobump fiatVersion (#4300)
  - chore(dependencies): Autobump fiatVersion (#4299)
  - chore(dependencies): Autobump korkVersion (#4298)
  - feat(orchestration): provide a way to allow only certain configured ad-hoc operations to be performed (#4195)
  - fix(stageExecution): In MJ stages find the correct authenticated user… (#4289)
  - fix(sql): Wrong indentation for rollback in database changelog (#4297)
  - chore(dependencies): Autobump fiatVersion (#4296)
  - feat(igor): Stop Jenkins job when job name has slashes in the job name (#4294)
  - fix(preconfiguredJobs): Resource requests on custom stage | Error: got "map", expected "string" (#4295)
  - chore(dependencies): Autobump korkVersion (#4291)
  - fix(clouddriver): fix property binding for Clouddriver (#4290)
  - chore(build): Build docker images for multiple architectures (#4288)
  - refactor(groovy): migrating Clouddriver services to Java (#4269)
  - chore(dockerfile): upgrade to latest alpine image (#4284)
  - chore(dependencies): Autobump fiatVersion (#4283)
  - chore(dependencies): Autobump korkVersion (#4282)
  - feat(webhook): Allow webhook retries for selected status codes (#4276)
  - chore(tests): redact some data in test (#4281)
  - fix(restart-pipeline) : CheckPrecondition doesn't evaluate expression correctly when upstream stages get restarted (#4278)
  - feat(orca): add Kustomize 4 support (#4280)
  - chore(dependencies): Autobump korkVersion (#4275)
  - chore(dependencies): Autobump korkVersion (#4273)
  - fix(tasks): Fix MonitorPipelineTask regression (#4271)
  - chore(dependencies): Autobump korkVersion (#4272)
  - fix(cfn): Fix detection of empty CloudFormation changesets (#4270)
  - chore(ci): Mergify - merge Autobumps on release-* (#4264)
  - fix(ci): fetch previous tag from git instead of API (#4263)
  - feat(stageExecution): supporting extra custom tags for stage execution metrics (#4255)
  - chore(dependencies): Autobump korkVersion (#4258)
  - chore(dependencies): Autobump korkVersion (#4257)
  - chore(ci): Upload halconfigs to GCS on Tag push (#4256)
  - fix(dependency): Issue of missing javax.validation and hibernate-validator dependencies while upgrading the spring cloud to Hoxton.SR12 in kork (#4254)
  - Fix for size (#4242)
  - chore(dependencies): Autobump korkVersion (#4252)
  - feat(build): bump dependencies for the given branch (#4247)

#### Spinnaker Clouddriver - 1.31.2

  - chore(dependencies): Autobump fiatVersion (#5943)
  - fix(metrics): revert metric names to pre-Java (#5936) (#5942)
  - chore(dependencies): don't create an autobump PR for halyard on a clouddriver release branch (#5677) (#5939)
  - chore(dependencies): Autobump korkVersion (#5938)
  - chore(dependencies): Autobump fiatVersion (#5912)
  - chore(dependencies): Autobump spinnakerGradleVersion (#5918)
  - chore(dependencies): Autobump fiatVersion (#5919)
  - chore(gha): update to docker/login-action@v2 to stay up to date (#5920)
  - chore(dependencies): Autobump korkVersion (#5921)
  - chore(dependencies): Autobump fiatVersion (#5922)
  - feat(gha): configure dependabot to keep github actions up to date (#5923)
  - chore(deps): bump actions/cache from 2 to 3 (#5926)
  - chore(deps): bump actions/checkout from 2 to 3 (#5924)
  - chore(gha): replace action for creating github releases (#5929)
  - chore(deps): bump peter-evans/repository-dispatch from 1 to 2 (#5925)
  - chore(deps): bump actions/setup-java from 2 to 3 (#5928)
  - chore(deps): bump docker/build-push-action from 3 to 4 (#5927)
  - chore(gha): replace deprecated set-output commands with environment files (#5930)
  - chore(deps): bump github/codeql-action from 1 to 2 (#5932)
  - chore(deps): bump google-github-actions/upload-cloud-storage from 0 to 1 (#5931)
  - chore(deps): bump google-github-actions/auth from 0 to 1 (#5933)
  - chore(dependencies): Autobump korkVersion (#5934)
  - chore(dependencies): Autobump korkVersion (#5935)
  - chore(dependencies): Autobump korkVersion (#5937)
  - fix(metrics): revert metric names to pre-Java (#5936)
  - chore(dependencies): Autobump korkVersion (#5944)
  - chore(dependencies): Autobump korkVersion (#5946)
  - fix(aws): standardize retry logic in LocalFileUserDataProvider.isLegacyUdf (#5947)
  - feat(kubernetes): skip checking and allow operations on all kinds (#5949)
  - chore(dependencies): Autobump spinnakerGradleVersion (#5951)
  - refactor(deprecation): remove deprecated gradle constructs/features from clouddriver in order to upgrade gradle 7 (#5950)
  - chore(dependencies): Autobump korkVersion (#5952)
  - fix(aws): ECS Service Tagging broken (#5954)
  - chore(dependencies): Autobump korkVersion (#5961)
  - chore(dependencies): Autobump fiatVersion (#5962)
  - fix(gce): remove the duplicate cache attribute "subnet" and update the test (#5977) (#5984)
  - fix(builds): Backport flag for installing aws cli (#6009)
  - chore(dependencies): Autobump korkVersion (#6010)
  - chore(dependencies): Autobump fiatVersion (#6011)
  - fix: Fix docker build in GHA by removing some of the GHA tools (#6033) (#6036)
  - fix(lambda): Lambda is leaking threads on agent refreshes.  remove the custom threadpool (#6048) (#6049)

#### Spinnaker Rosco - 1.31.2

  - fix(manifests/test): add org.junit.jupiter:junit-jupiter-engine as a test runtime dependency (#963)
  - chore(dependencies): Autobump spinnakerGradleVersion (#964)
  - chore(gha): update to docker/login-action@v2 to stay up to date (#965)
  - chore(gha): replace action for creating github releases (#966)
  - fix(gha): remove empty env block (#967)
  - fix(gha): remove refs/tags from github release names (#968)
  - chore(gha): use checkout@v3 to stay up to date (#969)
  - feat(gha): configure dependabot to keep github actions up to date (#970)
  - chore(deps): bump google-github-actions/auth from 0 to 1 (#972)
  - chore(deps): bump docker/build-push-action from 3 to 4 (#973)
  - chore(deps): bump google-github-actions/upload-cloud-storage from 0 to 1 (#971)
  - chore(dependencies): Autobump korkVersion (#974)
  - chore(dependencies): Autobump korkVersion (#975)
  - chore(dependencies): Autobump korkVersion (#976)
  - chore(dependencies): Autobump korkVersion (#977)
  - refactor(retrofit2): Use retrofit2.x client instead of retrofit1.9 for artifact fetch from clouddriver (#953)
  - refactor(web/test): V2BakeryControllerWithClouddriverServiceTest cleanup (#979)
  - chore(dependencies): Autobump korkVersion (#981)
  - refactor(retrofit2): use retrofit2 client to clouddriver API calls instead of retrofit1.9 (#980)
  - chore(dependencies): Autobump korkVersion (#982)
  - refactor(manifests): use new methods in manifest exception handling (#983)
  - chore(dependencies): Autobump spinnakerGradleVersion (#985)
  - chore(dependencies): Autobump korkVersion (#987)
  - chore(dependencies): Autobump korkVersion (#988)
  - chore(dependencies): Autobump korkVersion (#1014)

