### kubedemo
```
kubectl apply -f quickdemo
OR
kubectl apply -f quickdemo2
OR
helm create quickdemochart
helm upgrade --install --values=./helm/load-balancer-values.yaml quickdemochart quickdemochart
helm delete quickdemochart


What if i want to use ony docker?
docker run -p 8080:80 -d nginxdemos/hello:plain-text
docker run -p 8081:80 -d nginxdemos/hello

curl http://0.0.0.0:8080      curl http://localhost:8080
curl http://0.0.0.0:8081      curl http://localhost:8081/ 
```
