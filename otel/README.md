# Local Testing
Use this file to run collector locally and can see metrics and traces are published in the files 

Steps:
---
1.Download otelcontribcol_linux_amd64 from https://github.com/open-telemetry/opentelemetry-collector-contrib/releases/tag/v0.31.0

2. RUN -> 
$ otelcontribcol_linux_amd64 --config otel-collector-config.yaml


Logs:
---
2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:75 Starting GRPC server on endpoint 0.0.0.0:**4317**   {"kind": "receiver", "name": "otlp"}
2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:75 Starting GRPC server on endpoint 0.0.0.0:55680  {"kind": "receiver", "name": "otlp"}

2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:93 Starting HTTP server on endpoint 0.0.0.0:**4318**   {"kind": "receiver", "name": "otlp"}
2021-08-14T11:50:37.755Z        info    otlpreceiver/otlp.go:93 Starting HTTP server on endpoint 0.0.0.0:55681  {"kind": "receiver", "name": "otlp"}
