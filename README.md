# argocd-gitops

This repository contains GitOps configuration for deploying and managing Kubernetes applications using [Argo CD](https://argo-cd.readthedocs.io/) as the continuous delivery controller.

- **GitOps**: All desired cluster state is defined in this repository. Changes made are automatically applied to the cluster by Argo CD.
- **Argo CD App-of-Apps Pattern**: This repo uses a root "app-of-apps" Application to manage multiple child Applications (such as Istio and Flask app).


## Applications

- **Istio**  
  - Installs Istio CRDs, control plane, and gateway components.
  - Enables service mesh and ingress for workloads.
- **Flask App**  
  - Deploys a sample Python Flask application.
  - Uses Istio for ingress and traffic management.