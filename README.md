# kubeinvaders-manifests

This provides the Kubernetes manifests of [KubeInvaders](https://github.com/lucky-sideburn/KubeInvaders).

## Getting Started

You need to replace the domain name in the `Ingress` and `Deployment`.

Apply the manifests:

```sh
# Create a service account
kubectl apply -f namespace.yaml serviceaccount.yaml

# Find the secret and replace the name in deployment.yaml
kubectl -n kubeinvaders get secret | grep kubeinvaders-token
sed -e s/REPLACE_TOKEN_NAME/kubeinvaders-token-NAME/ deployment.yaml

# Apply
kubectl apply -f .
```
