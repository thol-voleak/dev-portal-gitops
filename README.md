# dev-portal-gitops

The GitOps repo for Dev Portal release management. The portal opens PRs that bump
`images[].newTag` in `apps/<namespace>/<deployment>/overlays/<env>/kustomization.yaml`,
and Argo CD deploys whatever is merged to `main`.

Locally every environment is a namespace (`payment-sit`, `payment-uat`, ...) in one minikube.
