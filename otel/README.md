# Local Testing
Use this file to run collector locally and can see metrics and traces are published in the files 

Steps:
---
1.Download otelcontribcol_linux_amd64 from https://github.com/open-telemetry/opentelemetry-collector-contrib/releases/tag/v0.31.0

2. RUN -> 
$ otelcontribcol_linux_amd64 --config otel-collector-config.yaml


OpenTelemetry Collector for DataDog:
---
https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/exporter/datadogexporter
https://github.com/open-telemetry/opentelemetry-collector-contrib/blob/main/exporter/datadogexporter/example/example_k8s_manifest.yaml


2021-08-15T21:35:06.280Z        info    service/collector.go:235        Loading configuration...
Error: cannot load configuration's parser: error loading config file "/conf/otel-collectorcollector-config.yaml": unable to read the file /conf/otel-collectorcollector-config.yaml: open /conf/otel-collectorcollector-config.yaml: no such file or directory
2021/08/15 21:35:06 collector server run finished with error: cannot load configuration's parser: error loading config file "/conf/otel-collectorcollector-config.yaml": unable to read the file /conf/otel-collectorcollector-config.yaml: open /conf/otel-collectorcollector-config.yaml: no such file or directory

Logs: (OTLP Port : 4317, 4318)
---
```
2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:75 Starting GRPC server on endpoint 0.0.0.0:4317   {"kind": "receiver", "name": "otlp"}
2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:75 Starting GRPC server on endpoint 0.0.0.0:55680  {"kind": "receiver", "name": "otlp"}

2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:93 Starting HTTP server on endpoint 0.0.0.0:4318   {"kind": "receiver", "name": "otlp"}
2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:93 Starting HTTP server on endpoint 0.0.0.0:55681  {"kind": "receiver", "name": "otlp"}
```
