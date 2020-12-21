# CloudCasa Kubernetes Agent

[CloudCasa](https://cloudcasa.io) - A Smart Home in the Cloud for Kubernetes Backups

## Introduction

CloudCasa is a SaaS solution that provides class-leading data protection services for Kubernetes and cloud native applications.

This chart installs and configures the CloudCasa agent on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.16+
- Helm 2.11+ or Helm 3.0+

## Installation

1. Log in to https://home.cloudcasa.io and add your Kubernetes cluster under the Setup tab. Note the returned cluster ID.
2. Go to charts. In Deploy Chart section, check the Partners checkbox and click on the cloudcasa-kubeagent chart.
3. Provide the App Name.
4. In cloudcasa setting section, provide the Obtained Cluster ID.
5. Click on the Install button.

## Uninstall
Application delete option is available in the Installed App section.

*CloudCasa is a trademark of Catalogic Software Inc.*
