Remove podinfo

> `kubectl delete all --all -n podinfo-app`

Deploy `cert-manager` using a helm chart at `https://charts.jetstack.io`

> `helm repo add jetstack https://charts.jetstack.io`
> 
> `helm install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace --version v1.3.1 --set installCRDs=true`