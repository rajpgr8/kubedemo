### kubedemo
```
kubectl apply -f quickdemo
OR
kubectl apply -f quickdemo2
OR
helm create quickdemochart
     Chart.yaml -> change 'appVersion -> latest'
     values.yaml -> change 'replicaCount -> 3', 'image.repository -> nginxdemos/hello', 'service.type -> LoadBalancer' (or NodePort)
helm upgrade --install quickdemochart quickdemochart
```
