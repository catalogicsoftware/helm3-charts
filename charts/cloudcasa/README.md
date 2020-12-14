# Cloudcasa
Cloudcasa is one of the most versatile SaaS solution to manage backups for your Kubernetes/Docker containers and Volumes.

## Introduction

This chart bootstraps a kubeagent deployment on a client Kuberntes [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager. This inturns registers the client Kubernetes cluster with Cloudcasa.

## Prerequisites

- Kubernetes 1.16+
- Helm 2.11+ or Helm 3.0+

## Helm Chart installation modes

### CLI based installation

```bash
1. helm repo add cloudcasa-repo https://catalogicsoftware.github.io/cloudcasa-helmchart
2. helm install cloudcasa.io cloudcasa-repo/cloudcasa-helmchart --set AMDS_CLUSTER_ID=<Cluster ID>
```
### Helmchart hosted on Rancher Apps

```
1. Go to charts, select the repo -> cloudcasa-kubeagent chart.
2. Provide the name of teh app.
3. In cloudcasa setting section, provide the AMDS_CLUSTER_ID.
4. Click on Install button.
```
