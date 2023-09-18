This week we'll learn about the Kafka storage tool. You can use it to generate a Cluster UUID and then
format the storage when you're [running Kafka in KRaft mode](https://docs.confluent.io/kafka/operations-tools/kafka-tools.html#kafka-storage-sh). 

First, you need to use the tool to generate a random UUID:

```
bin/kafka-storage.sh random-uuid
d5999679-ba23-4816-8363-0f67e28ae6e1
```

Using the tool ensures that it'll be a [type 4 UUID not matching](https://stackoverflow.com/questions/68581003/apache-kafka-kraft-kafka-storage-tool) the internal Kafka UUIDs. 

Next up, format your cluster with the id, passing in the path to your `server.properties`:

```
bin/kafka-storage.sh format -t d5999679-ba23-4816-8363-0f67e28ae6e1 -c config/kraft/server.properties
```

and that's it! 