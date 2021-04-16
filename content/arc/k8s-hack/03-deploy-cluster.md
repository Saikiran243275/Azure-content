---
title: "Deploy Cluster"
description: "Create unmanaged Kubernetes clusters ready for onboarding with Azure Arc."
slug: deploy-cluster
menu:
  side:
    parent: arc-k8s-hack
    identifier: arc-k8s-deploy-cluster
series:
 - arc-k8s-hack
weight: 3
---

## Background

*Persona: Cluster Administrator*

In order to realise the benefits of Azure Arc we must be managing multiple clusters at scale.

In our scenario we are running a global platform with clusters deployed in separate regions. Each must be deployed, updated and managed independently.

This is causing pain for platform, development and operations teams support the application because of complexity of rolling out updates and ensuring a consistent, secure baseline.

## Challenge 1

The purpose of this challenge is to ensure you are comfortable running actions and creating secrets within GitHub and managing resources using the Azure CLI or Portal.

By the end of the challenge you will have access to 3 unmanaged Kubernetes clusters.

> Since AKS is a 1st-party Azure solution and natively supports capabilities such as Azure Monitor integration as well as GitOps configurations (currently in preview), we must create unmanaged Kubernetes clusters.

### Cluster Creation

Create at least two on-premises Kubernetes clusters. (E.g. 'alpha', 'beta', 'gamma'.)

You are welcome to create these external clusters as you want, however the **team repository** that you previously cloned has a [GitHub action](https://devblogs.microsoft.com/premier-developer/github-actions-overview/) for deploying an unmanaged k3s cluster by Rancher to Azure.

> Hint: Read the README.md!

You could use any other [validated distribution](https://docs.microsoft.com/azure/azure-arc/kubernetes/validation-program#validated-distributions) if you're more comfortable.

## Success Criteria

* At least two unmanaged Kubernetes clusters are running
* You can get a list of nodes in **Ready** status by using `kubectl get node` for each cluster
* You can navigate to the public IP address for each cluster and view a 404 page since no applications are deployed

## References

* Using GitHub Actions to deploy Infrastructure
* Team respository README
* Traefik Ingress Controller
