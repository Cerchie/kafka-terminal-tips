Did you know there’s a way to check on your Confluent CLI plugins from the command line?

```
❯ confluent plugin list
```

This command provides a quick way to verify which plugins you have access to, as well as their file paths (which can help with troubleshooting):

```
   Plugin Name  |          File Path
----------------+-------------------------------
  confluent hub | /usr/local/bin/confluent-hub
```

You can find the code for other useful plugins, like `api-key-purge`, in [this GitHub repository](https://github.com/confluentinc/cli-plugins). We’d love to have contributors as well!
