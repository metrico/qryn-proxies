# Grafana Proxies
## Datadog to Prometheus

### Build
```
docker built -t datadog-proxy .
```

### Usage
```
docker run --rm -ti datadog-proxy {options}
```

#### Options
```
  -api.intake-timeout duration
        Sets /intake timeout, by default 5 seconds (default 5s)
  -api.v1-check-run-timeout duration
        Sets api/v1/check_run timeout, by default 5 seconds (default 5s)
  -api.v1-series-timeout duration
        Sets api/v1/series timeout, by default 5 seconds (default 5s)
  -api.v1-sketches-timeout duration
        Sets api/v1/sketches and api/beta/sketches timeout, by default 5 seconds (default 5s)
  -auth.enable
        require X-Scope-OrgId header (default true)
  -ht-cache-expiration duration
        Expiration for cached values. Zero means no expiration. Seconds precision will be used. Should be less than one month. (default 10m0s)
  -ht-cache-invalidation-retry-delay duration
        RetryDelay to retry cache invalidation if update fails after storing. Zero means disabled. Arbitrary precision. (default 1m0s)
  -instrument-buckets string
        Buckets for instrumentation, comma separated list of seconds as floats. (default ".005,.010,.015,.020,.025,.050,.100,.250,.500,1,2.5,5,10")
  -internalserver.graceful-shutdown-timeout duration
        Timeout for graceful shutdowns (default 5s)
  -internalserver.http-listen-address string
        Internal HTTP server listen address.
  -internalserver.http-listen-port int
        Internal HTTP server listen port. (default 8081)
  -memcached-max-idle-conns int
        Max idle conns for each memcached server. (default 5)
  -memcached-server value
        Memcache server to use, can be passed several times, consistent hashing will be used to distribute the keys.
  -memcached-timeout duration
        Timeout for memcached operations. (default 100ms)
  -query-endpoint string
        URL for queries from upstream Prometheus API.
  -query-keep-alive duration
        KeepAlive for queries to upstream Prometheus API. (default 30s)
  -query-max-conns int
        Max conns per host for queries to upstream Prometheus API. (default 100)
  -query-max-idle-conns int
        Max idle conns for queries to upstream Prometheus API. (default 10)
  -query-timeout duration
        Timeout for queries to upstream Prometheus API. (default 30s)
  -server.graceful-shutdown-timeout duration
        Graceful shutdown period (default 5s)
  -server.grpc-listen-port int
        Sets listen address port for the http server (default 9095)
  -server.http-listen-address string
        Sets listen address for the http server (default "0.0.0.0")
  -server.http-listen-conn-limit int
        Sets a limit to the amount of http connections, 0 means no limit
  -server.http-listen-port int
        Sets listen address port for the http server (default 8000)
  -server.http-max-req-size-limit int
        HTTP max request body size limit in MB (default 10485760)
  -server.http-server-idle-timeout duration
        HTTP request idle timeout (default 30s)
  -server.http-server-read-timeout duration
        HTTP request read timeout (default 30s)
  -server.http-server-write-timeout duration
        HTTP request write timeout (default 30s)
  -server.path-prefix string
        Base path to serve all API routes from (e.g. /v1/)
  -service-name string
        the service name used in traces
  -skip-label-validation
        If set to true sends requests with headers to skip label validation.
  -user-agent string
        User agent for proxy ingester
  -write-endpoint string
        URL for writes to upstream Prometheus remote write API (including the /push suffix if needed).
  -write-keep-alive duration
        KeepAlive for write to upstream Prometheus remote write API. (default 30s)
  -write-max-conns int
        Max open conns per host for writes to upstream Prometheus remote write API. (default 100)
  -write-max-idle-conns int
        Max idle conns per host for writes to upstream Prometheus remote write API. (default 10)
  -write-timeout duration
        Timeout for writes to upstream Prometheus remote write API. (default 1s)    
 ```
