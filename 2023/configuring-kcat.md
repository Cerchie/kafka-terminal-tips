USED SEP 19 23

Today we're going to talk about the different ways to configure [kcat](https://github.com/edenhill/kcat).

First of all, one of the reasons that kcat is so useful is that any piece of [librdkafka configuration](https://github.com/confluentinc/librdkafka/blob/master/CONFIGURATION.md) is available to it via the -X flag:

```
 kcat -b broker_name -t topic_name -X client.id=rdkafka
```

If you've got a lot of configuration and don't want to be passing them in every time you run the command, you can feed kcat a config file:

```
 kcat -b broker_name -t topic_name -X client -F ./path/to/config_file
```

If there's no config file set, kcat will consult `$KCAT_CONFIG` or, if you like, you can set configuration in a `~/.config/kcat.conf` file to avoid passing in any config values at all. 
