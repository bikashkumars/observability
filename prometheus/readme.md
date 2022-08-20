## Prerequisite

1. install Docker
2. Configure prometheus.yml as per your need
3. locate where you have saved prometheus.yml as you have to supply it to docker run command

## Start Prometheus

set the correct path of prometheus.yml file and supply it to docker run

/Users/bikash/Desktop/prometheus/prometheus.yml

```
docker run \
    -p 9090:9090 \
    -v /Users/bikash/Desktop/prometheus/prometheus.yml:/etc/prometheus/prometheus.yml \
    prom/prometheus
```

Now head to http://localhost:9090/ to Prometheus dashboard console

## Who will send data to Prometheus

First of all Prometheus it-self as a Software generates its own metrics which can be sent to Prometheus. By dault promethus already sending its own metrics to Prometheus.

If you want to see how prometheus own Metrics looks like

'''
http://localhost:9090/metrics
'''

If you want to send prometheus own metrics to prometheus, then you can do this

If you want to see those metrics on Prometheus


Go to http://localhost:9090/
In the expression textbox search for "promhttp_metric_handler_requests_total"
Press enter
