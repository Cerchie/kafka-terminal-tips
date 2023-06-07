Did you know you can use the Confluent CLI to [store your API keys](https://docs.confluent.io/confluent-cli/current/connect.html)? That way you can run subsequent commands against the cluster you specify with the key and you don't have to add it every time. This limits exposure. 

Here's how you'd set that up:

```
confluent api-key use <api-key> --resource <resource-id>
```

