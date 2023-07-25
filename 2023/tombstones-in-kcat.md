USED AUG 23

Let's talk about the `-Z` flag in kcat for a moment.

This is a very special flag. As you can see from its [definition](https://github.com/edenhill/kcat/blob/ab6ce814fa2e435359e77a1d3813853248679206/kcat.h#L100) in the code, it will interpret empty message values as `null`. What's important about that? Well, it enables us to set up [tombstones](https://medium.com/@damienthomlutz/deleting-records-in-kafka-aka-tombstones-651114655a16) via kcat:

```
echo "key_of_events_to_remove:" | kcat -b broker_name -t topic_name -Z -K:
```

Here, you pipe the name of the key you want removed directly into kcat, the `-Z` flag ensures that the empty message is interpreted as null and therefore becomes a tombstone. FYI, the `-K` flag is the key delimiter. 
