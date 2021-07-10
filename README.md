### kubedemo
```
kubectl apply -f quickdemo
OR
kubectl apply -f quickdemo2
OR
helm create quickdemochart
helm upgrade --install --values=./helm/load-balancer-values.yaml quickdemochart quickdemochart
helm delete quickdemochart
```
