```bash
TODO: set the dns name of the vm
LOCATION=uksouth
scp arcdemo@HOSTNAME.$LOCATION.cloudapp.azure.com:~/.kube/config ~/.kube/blah-$LOCATION.config
```


```bash
LOCATION=uksouth
az connectedk8s connect --name arc4k8s-$LOCATION --resource-group arc4k8s
LOCATION=westeurope
az connectedk8s connect --name arc4k8s-$LOCATION --resource-group arc4k8s
```
