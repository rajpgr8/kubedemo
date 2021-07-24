### kubedemo
```
With Docker:
-----------
docker run -p 8080:80 -d nginxdemos/hello:plain-text
docker run -p 8081:80 -d nginxdemos/hello

curl http://0.0.0.0:8080      curl http://localhost:8080
curl http://0.0.0.0:8081      curl http://localhost:8081/ 


With Kubernetes:
---------------
kubectl apply -f quickdemo      (using ingress)
OR
kubectl apply -f quickdemo2     (using LB)
OR
helm create quickdemochart
helm upgrade --install --values=./helm/load-balancer-values.yaml quickdemochart quickdemochart
helm delete quickdemochart

```

with pulumi:
-----------
```
cd quickdemo_pulumi
pulumi up --yes

Code Reference: https://www.pulumi.com/docs/tutorials/kubernetes/gke/
```
