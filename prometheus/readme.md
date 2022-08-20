## Start Prometheus

set the correct path of prometheus.yml file and supply it to docker run

/Users/bikash/Desktop/prometheus/prometheus.yml

```
docker run \
    -p 9090:9090 \
    -v /Users/bikash/Desktop/prometheus/prometheus.yml:/etc/prometheus/prometheus.yml \
    prom/prometheus
```