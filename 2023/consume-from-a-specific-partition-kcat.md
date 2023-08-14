You can use kcat https://github.com/edenhill/kcat to consume from a specific partition, rather than the default, which is all the
partitions in the topic. 

```
❯ kcat -t topicname -C -p 0

% Reached end of topic topicname [0] at offset 902
```

From the example above, you can see that the way to consume from a specific partition is 
to use the `-p` flag followed by the number of the partiion you want to consume from. 

