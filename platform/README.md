# Platform

These are platform-level services that are required for cluster operations. Nothing in here should
be applied directly to the cluster. Instead, the `kustomization` in `bootstrap` should be applied.
This will install argocd and its pre-requisites into the cluster. From there, argocd will take over
managing itself and the other bootstrapped services. It will also begin installing all the other
services to the cluster.

## Bootstrapping Services

Currently, this is:

1. cert-manager
2. ingress-nginx
3. argocd

Technically we could get away with just argocd, but I wanted ingress to be up before argo, so we can use the UI for troubleshooting.

## Other Services

1. External-dns
2. ???
