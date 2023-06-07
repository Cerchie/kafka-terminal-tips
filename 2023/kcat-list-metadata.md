What if you want to list metadata from your Kafka cluster, topics, partitions, replicas and in-sync replicas? 

You can run a command with the `-L` and `-J` flags:

```
kcat -b mybrokeraddress -L -J
```

`-L` is for list mode, and `-J` ensures JSON output. 

The output will look like:

```
 6 topics:
  topic "pksqlc-qqm92-processing-log" with 8 partitions:
    partition 0, leader 4, replicas: 4,9,2, isrs: 9,4,2
    partition 1, leader 8, replicas: 8,10,0, isrs: 0,10,8
    partition 2, leader 6, replicas: 6,11,4, isrs: 6,4,11
    partition 3, leader 7, replicas: 7,3,8, isrs: 3,7,8
    ...etc
```

