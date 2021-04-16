---
title: "Deploy Application"
description: "Run an application with Azure resource dependencies."
slug: "deploy-an-application"
menu:
  side:
    parent: arc-k8s-hack
    identifier: arc-k8s-deploy-app
series:
 - arc-k8s-hack
weight: 6
---

## Background

*Persona - Developer*
*Persona - Cluster Administrator*

Your development team want to deploy a new application version into all connected clusters.

This is the flagship review application that currently is running in a number of locations. It requires access to **Azure Storage** and an **Azure SQL Database**.

## Challenge

**TODO: Ensure that subscriptions are provisioned with appropriate resources / GH Action exists to provision them** 

Deploy the extra infrastructure resources using a GitHub action.

Have the cluster administrator deploy a cluster wide certificate issuer from Lets Encrypt.

Deploy the application using a GitOps approach and configure access to Azure resources using Managed Identities.

## Success Criteria

* Review application is running on all your clusters
* You can sign in, leave a review and upload an image

## References

* [Use Helm with Azure Arc for Kubernetes](https://docs.microsoft.com/azure/azure-arc/kubernetes/use-gitops-with-helm#overview-of-using-gitops-and-helm-with-azure-arc-enabled-kubernetes)

* [Managed Identity](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview)

* [Deploy Azure Resources](https://github.com/jasoncabot-ms/arc-for-kubernetes)