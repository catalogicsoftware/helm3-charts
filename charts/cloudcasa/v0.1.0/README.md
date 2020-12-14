# CloudCasa Kubernetes Agent

## Introduction

[CloudCasa](https://cloudcasa.io) is a class-leading SaaS solution providing data protection services for Kubernetes and cloud native applications.

This chart installs and configures the CloudCasa agent on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.16+
- Helm 2.11+ or Helm 3.0+

## Helm installation methods

### Installation using Rancher Apps Repository

1. Log in to https://home.cloudcasa.io and add your Kubernetes cluster under the Setup tab. Note the cluster ID.
2. Log in to the Rancher UI and go to charts and select the repo -> Cloudcasa-kubeagent chart.
3. Provide the release/app name.
4. In the cloudcasa settings section, enter the AMDS_CLUSTER_ID provided by CloudCasa in step 1.
5. Click on the Install button

### Installation via Helm CLI

1. Log in to https://home.cloudcasa.io and add your Kubernetes cluster under the Setup tab. Note the cluster ID.
2. Execute the following helm commands:
```
  helm repo add cloudcasa-repo https://catalogicsoftware.github.io/cloudcasa-helmchart
  helm install cloudcasa.io cloudcasa-repo/cloudcasa-helmchart --set AMDS_CLUSTER_ID=<Cluster ID>
```

## Uninstalling via Helm CLI

To uninstall/delete the `cloudcasa.io` deployment:

```
  helm delete cloudcasa.io
```

*CloudCasa is a trademark of Catalogic Software Inc.*

