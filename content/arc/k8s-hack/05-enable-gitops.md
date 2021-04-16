---
title: "Enable GitOps"
description: "An operating model for building cloud native applications."
slug: "enable-gitops"
menu:
  side:
    parent: arc-k8s-hack
    identifier: arc-k8s-enable-gitops
series:
 - arc-k8s-hack
weight: 5
---

## Background

*Persona: Cluster Admin - Cluster Repository*

*Persona: Developer - Development Repository*


GitOps works by using Git as a single source of truth for declarative infrastructure and applications.

Your cluster monitors and automatically updates itself to reconciles differences between current and desired state.

With Git at the center of your delivery pipelines, developers use familiar tools to make pull requests to accelerate and simplify both application deployments and operations tasks to Kubernetes.

This allows you to write once and deploy many times to identical clusters.

## Challenge

Deploy an application to your cluster(s) without running `kubectl`

A [sample application](/arc/k8s-hack/assets/podinfo.yaml) manifest has been provided that will show information and allow you to access certain functions. This manifest will shouldn't require any changes before being deployed.

You will have to set up [namespaces and RBAC](https://docs.microsoft.com/azure/azure-arc/kubernetes/tutorial-use-gitops-connected-cluster#create-a-configuration) before deploying the application. This should be done as the cluster administrator.

Discuss the advantage and disadvantages of using a GitOps approach, you may want to touch on delivering updates, managing multiple clusters, secrets management, security and access management and the benefits of having multiple source code repositories.

* **Stretch** Can you set it up to talk to a private GitHub repository?

## Success Criteria

* The sample application is running on your cluster and is publicly accessible

## References

* [What is GitOps - WeaveWorks?](https://www.weave.works/technologies/gitops/)
* [podinfo](https://github.com/stefanprodan/podinfo)
* [Enable GitOps](https://docs.microsoft.com/azure/azure-arc/kubernetes/tutorial-gitops-ci-cd#connect-the-gitops-repo)
* [namespaces and RBAC](https://docs.microsoft.com/azure/azure-arc/kubernetes/tutorial-use-gitops-connected-cluster#create-a-configuration)