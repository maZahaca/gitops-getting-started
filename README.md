# gitops-getting-started
This repo contains guidance on how to start utilizing GitOps best practices with a Kubernetes cluster.
Define the GitOps term!

## Environment
1. Existing Kubernetes cluster in cloud provider [e.g. DigitalOcean]
2. Git repository for representing a state of Kubernetes applications.

## Goals
1. Allow team members to deploy applications more easily than nothing to the staging/dev environment.
2. Deploy from a branch.

## Non-goals
1. Eear money

## Process
- [ ] Gain access to Kubernetes cluster by getting [kubeconfig](https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/)
- [ ] Configure kube config and check access to the cluster by the command `kubectl get pods --all-namespaces` should return something
- [ ] Install [argocd](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- [ ] Make argocd accessible from the internet and issue an SSL certificate for it
- [ ] Add access via third-party provider
  - [ ] Github, Github groups (prod-deployers)
- [ ] Organize Github structure for argocd
  - [ ] apps - argocd applications 
  - [ ] charts - helm charts
  - [ ] values - values for the charts for specific env
- [ ] Add kubernetes cluster into argocd (? should be added by default the one where argocd is installed).
- [ ] Connect argocd to the git repository
- [ ] Make tests of deployments
