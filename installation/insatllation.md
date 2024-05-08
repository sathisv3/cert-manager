Cert-manager Installation
=========================
### helm repo add
### For reference https://cert-manager.io/docs/installation/helm/
helm repo add jetstack https://charts.jetstack.io --force-update

### helm repo update
 '''console
 helm repo update 
'''
### Install CRDs with kubectl 
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.14.5/cert-manager.crds.yaml

# Install cert-manager with helm 
helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --version v1.14.5 \
  # --set installCRDs=true

### for more reference 
### https://technotim.live/posts/kube-traefik-cert-manager-le/


Reflector Installation
======================



