FROM golang:alpine as builder
RUN apk add git make bash
WORKDIR /
RUN git clone https://github.com/grafana/mimir-proxies
WORKDIR /mimir-proxies
RUN  go mod tidy && make build

FROM alpine:3.11.3
COPY --from=builder /mimir-proxies/dist/graphite-proxy-writes .
EXPOSE 8009
ENTRYPOINT [ "./graphite-proxy-writes" ]
