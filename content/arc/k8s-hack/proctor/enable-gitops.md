Ensure that you repository is public
Ensure that you're doing over HTTPS

```bash
az k8s-configuration create \
    --name cluster-config \
    --cluster-name arc4k8s-uksouth \
    --resource-group arc4k8s \
    --operator-instance-name cluster-config \
    --operator-namespace cluster-config \
    --operator-params='--git-readonly --sync-garbage-collection --git-branch=main --git-path=cluster-config' \
    --repository-url https://github.com/jasoncabot-ms/arc-for-kubernetes \
    --scope cluster \
    --cluster-type connectedClusters
```