Cert-manager Installation
=========================
### helm repo add
### For reference https://cert-manager.io/docs/installation/helm/
helm repo add jetstack https://charts.jetstack.io --force-update

### helm repo update
 '''sh
 helm repo update 

### Install CRDs with kubectl 
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.14.5/cert-manager.crds.yaml

### Install cert-manager with helm 
helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --version v1.14.5 \
  #--set installCRDs=true

### for more reference 
### https://technotim.live/posts/kube-traefik-cert-manager-le/


Reflector Installation
======================

Reflector is a Kubernetes addon designed to monitor changes to resources (secrets and configmaps) and reflect changes to mirror resources in the same or other namespaces.Since secrets and configs are scoped to a single namespace, this helps you create and change resources in one namespace and “reflect” them to resources in other namespaces.This is especially helpful for things like certificates and configs that are needed in multiple namespaces.You can find the GitHub repo here!




