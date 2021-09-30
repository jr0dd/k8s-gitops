<div align="center">

<img src="https://camo.githubusercontent.com/5b298bf6b0596795602bd771c5bddbb963e83e0f/68747470733a2f2f692e696d6775722e636f6d2f7031527a586a512e706e67" align="center" width="144px" height="144px"/>

 ### My home Kubernetes cluster :sailboat:

 _... managed with Flux and Renovate_ :robot:

 </div>

 <br/>

 <div align="center">

 [![k3s](https://img.shields.io/badge/k3s-v1.21.5-brightgreen?style=for-the-badge&logo=kubernetes&logoColor=white)](https://k3s.io/)
 [![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white&style=for-the-badge)](https://github.com/pre-commit/pre-commit)
 [![renovate](https://img.shields.io/badge/renovate-enabled-brightgreen?style=for-the-badge&logo=renovatebot&logoColor=white)](https://github.com/renovatebot/renovate)

</div>

---
## :book:&nbsp; Overview

This is home to my personal Kubernetes cluster. [Flux](https://github.com/fluxcd/flux2) watches this Git repository and makes the changes to my cluster based on the manifests in the [cluster](./cluster/) directory. [SOPS](https://toolkit.fluxcd.io/guides/mozilla-sops/) protects my secrets so I can keep everything on a public repo.

Currently I only have a single node with this running on TrueNAS SCALE. Which I am in the process of prepping for migration to Ubuntu for all teh freedoms. If you use this repo to install on TrueNAS be prepared for some manual intervention since their middleware prevents certain system changes to persist updates and/or reboots. Please see the truenas.sh script in the [hack](./hack) directory. I disabled the bundled [openebs-zfs-localpv](https://github.com/openebs/zfs-localpv) so I had more freedom with updates by using the helm chart.

For more information, head on over to my [docs](https://jr0dd.github.io/k8s-gitops/). ***Not ready yet***

## Prometheus Rules
All my prometheus recording/alerting rules found in this repo can be found in my [prometheus-rules](https://github.com/jr0dd/prometheus-rules) repo.

## :handshake:&nbsp; Community

Thanks to all the people who donate their time to the [k8s@home](https://github.com/k8s-at-home/) community.
This repo would not exist if it wasn't for their work.

If you want to learn more start with this template [here](https://github.com/k8s-at-home/template-cluster-k3s/)
