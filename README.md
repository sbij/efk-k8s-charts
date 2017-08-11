# k2-charts

Launch the charts with:
```
helm dep update central-logging
helm install --namespace kube-logging -n alogs central-logging
```

These charts use a Kubernetes Daemonset that you can find here: [sbij/fluentd-kubernetes-daemonset](https://github.com/sbij/fluentd-kubernetes-daemonset).


Monitor your setup with:
```
watch kubectl get all,secret --namespace kube-logging
````

Delete your setup with:
```
kubectl delete namespace kube-logging
```

In case of problems:
```
kubectl -n kube-system get events
```
