# Hello GitOps

Example project to demonstrate GitOps using [Kustomize](https://github.com/kubernetes-sigs/kustomize), Harness CIE and Harness CD

- [What we want to achieve](#what-we-want-to-achieve)

## What we want to achieve

1. Code change is made to a Go application and pushed to main
2. Harness CIE pipeline is triggered
3. Code is first unit tested
4. If tests are OK, the application is packaged as a Docker image and pushed to DockerHub
5. The kustomize manifests are edited to reference this new image tag
6. Kustomize changes are committed and pushed automatically by the workflow
7. As kustomize files have changed, Harness Gitops synchronize the application state with the Kubernetes cluster to deploy or update the app
