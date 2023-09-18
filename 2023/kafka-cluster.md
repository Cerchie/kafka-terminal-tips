Let's say you wanted to retrieve the ID of one of your clusters, perhaps in order to [unregister](https://docs.confluent.io/kafka/operations-tools/kafka-tools.html#kafka-cluster-sh) it, or for working with [the metadata shell](https://docs.confluent.io/kafka/operations-tools/kafka-tools.html#kafka-metadata-shell-sh).

Well, `kafka-cluster` offers a way:

```
bin/kafka-cluster.sh cluster-id --bootstrap-server localhost:9092

Cluster ID: rjfRG-f1345lk3DUTO9plk
```
