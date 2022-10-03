# Grafana Proxies
## Datadog to Prometheus
### Usage
```
  -auth.enable=false \
  -server.http-listen-address 127.0.0.1 \
  -server.http-listen-port 8008 \
  -write-endpoint http://localhost:9009/api/v1/push
```
