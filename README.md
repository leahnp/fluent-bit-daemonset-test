# Fluent-Bit Daemonset for Kubernetes

Run [Fluent-Bit](http://fluentbit.io/) to collect logs and output them to elasticsearch in a Kubernetes cluster. Fluent-Bit is configured in this example to tail all containers (excluding Fluent-Bit containers) and collect STDERR/STDOUT logs made available at /var/log/containers/*.log by Docker.

## Usage

To deploy in a Kubernetes cluster:

```kubectl -f create fluent-bit-daemonset-elasticsearch.yaml```

[Elasticsearch for Kubernetes](https://github.com/kubernetes/kubernetes/tree/master/examples/elasticsearch)

## History

Previously we used FluentD as a log collector and are experimenting with this light-weight Fluent-Bit option. More details on our epxerience to come. 