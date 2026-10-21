# RKE2 project GitOps manifests

Kubernetes desired state for the rke2-project Flask app in namespace dev.
Application code, Dockerfile, tests and Jenkins CI live in:
https://github.com/hassanad72/rke2-project

Argo CD source settings after repository access is configured:
- Repository: git@github.com:hassanad72/rke2-project-gitops.git
- Revision: main
- Path: k8s
- Destination: https://kubernetes.default.svc
- Namespace: dev
- Sync policy: manual initially

Update the image in k8s/deployment.yaml to a successfully published ECR commit tag.
Jenkins write-back automation has not been configured yet.
Repository preparation does not change the live cluster or Argo CD Application.
