kcat https://docs.confluent.io/platform/current/clients/kafkacat-usage.html starts with a couple of defaults to know about. 

First of all, it automatically uses consumer mode:

```
❯ kcat -t topic_name
% Auto-selecting Consumer mode (use -P or -C to override)
```

If you want to run it in Producer mode, use `-P`, as indicated in the output.

Second, the default delimiter is newline:

```
 kcat -t topic_name
% Auto-selecting Consumer mode (use -P or -C to override)
{"key":"value": ["string"]}
{"key":"value": ["string"]}
```

If you'd like to use a delimiter, add `-K` with your desired delimiter.