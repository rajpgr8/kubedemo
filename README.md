### kubedemo
```
With Docker:
-----------
docker run -p 8080:80 -d nginxdemos/hello:plain-text
docker run -p 8081:80 -d nginxdemos/hello

curl http://0.0.0.0:8080      curl http://localhost:8080
curl http://0.0.0.0:8081      curl http://localhost:8081/ 

Note: can use this java repo for learning  & buidling image 
https://github.com/codefresh-contrib/gradle-sample-app  (gcr.io/<PROJECT_ID>/java:0.1)


With Kubernetes:
---------------
kubectl apply -f quickdemo      (using ingress)
OR
kubectl apply -f quickdemo2     (using LB)
OR
helm create quickdemochart
helm upgrade --install --values=./helm/load-balancer-values.yaml quickdemochart quickdemochart
helm delete quickdemochart


with pulumi (create cluster and deploy):
-----------
cd quickdemo_pulumi
npm install
pulumi config set gcp:project <PROJECT ID> 
pulumi up --yes

Code Reference: https://www.pulumi.com/docs/tutorials/kubernetes/gke/
```

```
Just for reference, do not use it without understanding properly:
https://signoz.io/blog/opentelemetry-spring-boot/ (can see how to build java Spring Boot app using maven and run it locally)
curl -L https://github.com/open-telemetry/opentelemetry-java-instrumentation/releases/latest/download/opentelemetry-javaagent-all.jar --output opentelemetry-javaagent-all.jar
OTEL_METRICS_EXPORTER=none OTEL_EXPORTER_OTLP_ENDPOINT="http://localhost:4317" OTEL_RESOURCE_ATTRIBUTES=service.name=javaApp java -javaagent:./opentelemetry-javaagent-all.jar -jar target/*.jar

can download collector agent with datadog
https://docs.datadoghq.com/tracing/setup_overview/open_standards/
```
