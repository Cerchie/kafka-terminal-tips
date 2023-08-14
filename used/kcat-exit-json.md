USED JUL 27, 23
Today we have a couple of quick usability tips for [kcat](https://github.com/edenhill/kcat).

Sometimes, when you're running kcat, you won't want it to be open in the background, you just want to run a command and read the result. In that case, you can add an `-e` flag to exit, in this case, after printing the last 300 lines from partition 2: 

```
$ kcat -C -b broker_name -t topic_name -p 2 -o -300-e
```

You can also view messages in JSON with a `-J` flag:

```
$ kcat -b broker_name -t topic_name -J
```
