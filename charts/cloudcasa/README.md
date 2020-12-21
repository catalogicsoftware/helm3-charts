# CloudCasa Kubernetes Agent

[CloudCasa](https://cloudcasa.io) - A Smart Home in the Cloud for Kubernetes Backups

## Introduction

CloudCasa is a SaaS solution that provides class-leading data protection services for Kubernetes and cloud native applications.

This chart installs and configures the CloudCasa agent on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.16+
- Helm 2.11+ or Helm 3.0+

## Installation

### Helmchart hosted on Rancher Apps

1. Go to charts, select the repo -> cloudcasa-kubeagent chart.
2. Provide the name of the app.
3. In cloudcasa setting section, provide the Cluster ID.
4. Click on the Install button.

### Helmchart CLI Installation

1. Log in to https://home.cloudcasa.io and add your Kubernetes cluster under the Setup tab. Note the returned cluster ID.
2. Execute the following helm commands, replacing ```<ClusterID>``` with the ID obtained above:
```
  helm repo add cloudcasa-repo https://catalogicsoftware.github.io/cloudcasa-helmchart
  helm install cloudcasa.io cloudcasa-repo/cloudcasa-helmchart --set cluster_id=<Cluster ID>
```
3. See the CloudCasa [Getting Started Guide](https://cloudcasa.io/get-started) for more information.

*CloudCasa is a trademark of Catalogic Software Inc.*
