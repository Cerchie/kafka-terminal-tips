If you're using the Confluent CLI, you may want to know how many plugins you've got installed. You can check that with
the `confluent plugin list` command:

```
❯ confluent plugin list
   Plugin Name  |            File Path             
----------------+----------------------------------
  confluent hub | /opt/homebrew/bin/confluent-hub  
```

You can also specify the format (`human`, `json`, or `yaml`) using the `o` flag: 

```
❯ confluent plugin list -o=json
[
  {
    "plugin_name": "confluent hub",
    "file_path": "/opt/homebrew/bin/confluent-hub"
  }
]
```