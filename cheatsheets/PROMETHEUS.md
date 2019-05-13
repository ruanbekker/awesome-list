## Resources:

- [Prometheus](https://prometheus.io/docs/querying/basics/)
- [PromQL for Beginners](https://medium.com/@valyala/promql-tutorial-for-beginners-9ab455142085)
- [Biggest Metrics](https://www.robustperception.io/which-are-my-biggest-metrics)
- [Top Metrics](https://github.com/grafana/grafana/issues/6561)
- [Ordina-Jworks](https://ordina-jworks.github.io/monitoring/2016/09/23/Monitoring-with-Prometheus.html)
- [Infinity Works](https://github.com/infinityworks/prometheus-example-queries)


## Examples:

Amount of Memory Available:

```
node_memory_MemAvailable_bytes
```

Amount of Memory Available in MB:

```
node_memory_MemAvailable_bytes/1024/1024
```

Amount of Memory Available in MB 10 minutes ago:

```
node_memory_MemAvailable_bytes/1024/1024 offset 10m
```

Average Memory Available for Last 5 Minutes:

```
avg_over_time(node_memory_MemAvailable_bytes[5m])/1024/1024
```

Histogram:

```
histogram_quantile(1.00, sum(rate(prometheus_http_request_duration_seconds_bucket[5m])) by (handler, le)) * 1e3
```

Number of Nodes (Up):

```
count(up{job="cadvisor_my-swarm"})
```

HAProxy Response Codes:

```
haproxy_server_http_responses_total{backend=~"$backend", server=~"$server", code=~"$code", alias=~"$alias"} > 0
```

Metrics with the most resources:

```
topk(10, count by (__name__)({__name__=~".+"}))
```

the same, but per job:

```
topk(10, count by (__name__, job)({__name__=~".+"}))
```

or jobs have the most time series:

```
topk(10, count by (job)({__name__=~".+"}))
```

Top 5 per value:

```
sort_desc(topk(5, aws_service_costs))
```

Table - Top 5 (enable instant as well):

```
sort(topk(5, aws_service_costs))
```

Group per Day (Table) - wip

```
aws_service_costs{service=~"$service"} + ignoring(year, month, day) group_right
  count_values without() ("year", year(timestamp(
    count_values without() ("month", month(timestamp(
      count_values without() ("day", day_of_month(timestamp(
        aws_service_costs{service=~"$service"}
      )))
    )))
  ))) * 0
```
