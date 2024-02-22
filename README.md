# GitOps Getting Started
This repo contains guidance on how to start utilizing GitOps best practices with a Kubernetes cluster.
Define the GitOps term!

## Environment
1. Existing Kubernetes cluster in cloud provider [e.g. DigitalOcean]
2. Git repository for representing a state of Kubernetes applications.

## Goals
1. Allow team members to deploy applications to the staging/dev environment more easily than nothing.
2. Deploy from a branch.
3. Record a video describing the process of setting up GitOps env.

## Non-goals
1. Earn money

## Process
- [ ] Gain access to Kubernetes cluster by getting [kubeconfig](https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/)
- [ ] Configure kube config and check access to the cluster by the command `kubectl get pods --all-namespaces` should return something
- [ ] Install [argocd](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- [ ] Make ArgoCD accessible from the internet and issue an SSL certificate for it
- [ ] Add access via third-party provider
  - [ ] Github, Github groups (prod-deployers)
- [ ] Organize Github structure for ArgoCD
  - [ ] apps - ArgoCD applications 
  - [ ] charts - helm charts
  - [ ] values - values for the charts for specific env
- [ ] Add kubernetes cluster into argocd (? should be added by default the one where argocd is installed).
- [ ] Connect ArgoCD to the git repository
- [ ] Make tests of deployments

## Tools
1. [Kubefirst - one to-go tool for fast setup of everything needed for GitOps](https://kubefirst.io)
2. [Kratix - a contract-based tool to establish a connection between application and infrastructure teams](https://www.kratix.io)
3. [Backstage - open platform for building developer portals](https://github.com/backstage/backstage)
