# CloudCasa Kubernetes Agent

[CloudCasa](https://cloudcasa.io) - A Smart Home in the Cloud for Kubernetes Backups

# Introduction

CloudCasa is a SaaS solution that provides class-leading data protection services for Kubernetes and cloud native applications. This chart installs and configures the CloudCasa agent on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.
See the CloudCasa [Getting Started Guide](https://cloudcasa.io/get-started) for more information.

## Prerequisites

1. Kubernetes 1.17+
2. Helm 2.11+ or Helm 3.0+

## Installation

### Helmchart hosted on Rancher Apps

1. Log in to https://home.cloudcasa.io and add your Kubernetes cluster under the Setup tab. Note the returned cluster ID.
2. Go to charts. In the Deploy Chart section, check the Partners checkbox and click on the cloudcasa-kubeagent chart.
3. Provide the App Name.
4. In the CloudCasa settings section, provide the Obtained Cluster ID.
5. Click on the Install button. This will install CloudCasa kubeagent on the Kubernetes cluster. 

### Helmchart CLI Installation

1. Log in to https://home.cloudcasa.io and add your Kubernetes cluster under the Setup tab. Note the returned cluster ID.
2. Execute the following helm commands, replacing ```<ClusterID>``` with the Cluster ID obtained above:
```
$ helm repo add cloudcasa-repo https://catalogicsoftware.github.io/cloudcasa-helmchart
$ helm install cloudcasa.io cloudcasa-repo/cloudcasa-helmchart --set cluster_id=<Cluster ID>
```
This will automatically install the CloudCasa Kubeagent whcih register the Kubernetes cluster with CloudCasa Server.

### Update CloudCasa
Execute the below commands to update the Helmchart.
```
$ helm repo update
$ helm upgrade cloudcasa.io cloudcasa-repo/cloudcasa-helmchart --set cluster_id=<Cluster ID>
```

### Uninstall CloudCasa
```
$ helm uninstall cloudcasa.io
```

*CloudCasa is a trademark of Catalogic Software Inc.*
