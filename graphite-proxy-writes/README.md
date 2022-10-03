# Grafana Proxies
## Graphite to Prometheus

### Build
```
docker built -t graphite-proxy .
```

### Usage
```
docker run --rm -ti graphite-proxy {options}
```

#### Options
```
  -auth.enable=false \
  -server.http-listen-address 127.0.0.1 \
  -server.http-listen-port 8008 \
  -write-endpoint http://localhost:9009/api/v1/push
```
