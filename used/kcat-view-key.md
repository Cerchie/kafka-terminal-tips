USED AUG 23

Today's tip example comes from the [Confluent Docs](https://docs.confluent.io/platform/current/clients/kafkacat-usage.html). 

If you'd like to view your message keys outputted in kcat, add a `-K` flag with a delimiter:

```
 kcat -b localhost:9092 -t mysql_users -C -c1 -K\t
1   {"uid":1,"name":"Cliff","locale":"en_US","address_city":"St Louis","elite":"P"}
```

Want to know what a delimiter is? Consult [this article](https://www.computerhope.com/jargon/d/delimite.htm) which gives a general definition.
