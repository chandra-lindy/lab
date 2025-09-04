# pod related kubectl commands

## create & update

```bash
kubectl run <pod-name> --image <image-name>

kubectl run <pod-name> --image=<image-name> --dry-run=client -o yaml > pod.yaml
kubectl create -f pod.yaml --save-config
kubectl apply -f pod.yaml

kubectl get pod <pod-name> -o yaml > pod.yaml
kubectl edit pod <pod-name>
kubectl replace -f pod.yaml --force
```

## inspect

```bash
kubectl get pods
kubectl get pods -o wide
kubectl describe pods <pod-name>
kubectl get pods -o yaml
```

## delete

```bash
kubectl delete pod <pod-name>
kubectl delete -f pod.yaml
kubectl delete pods --all
```

## troubleshooting

```bash
kubectl logs <pod-name>
kubectl exec -it <pod-name> -- /bin/sh
```
