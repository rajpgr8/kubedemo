### kubedemo
```
kubectl apply -f quickdemo
OR
kubectl apply -f quickdemo2


helm create quickdemochart
Chart.yaml -> change 'appVersion'
values.yaml -> change 'replicaCount', 'image.repository', 'service.type' (to LoadBalancer or NodePort)
helm upgrade --install quickdemochart quickdemochart
```
