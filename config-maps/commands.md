# config map related kubectl commands

## create & update

```bash
kubectl create cm <configmap-name> --from-file=<file-path> --from-file=<file-path>
kubectl create cm <configmap-name> --from-file=<file-path> --from-literal=<key>=<value>

kubectl create cm <configmap-name> --from-literal=<key>=<value> --dry-run=client -o yaml > configmap.yaml
kubectl create -f cm.yaml --save-config
kubectl apply -f cm.yaml

kubectl get cm <configmap-name> -o yaml > configmap.yaml
kubectl edit cm <configmap-name>
kubectl replace -f cm.yaml --force
```

## inspect

```bash
kubectl get cm <configmap-name>
kubectl describe cm <configmap-name>
```

## delete

```bash
kubectl delete cm <configmap-name>
kubectl delete -f cm.yaml
```
