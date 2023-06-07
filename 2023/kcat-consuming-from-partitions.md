Did you know that when you use kcat without a `-p` flag you'll consume from all available partitions?

```
% kcat -C -b mybroker -t ais
% Reached end of topic ais [0] at offset 8378
% Reached end of topic ais [2] at offset 7959
% Reached end of topic ais [3] at offset 7523
% Reached end of topic ais [5] at offset 9261
% Reached end of topic ais [4] at offset 9137
```

What if you wanted to only consume from one partition? The `-p` flag comes in handy:

```
❯ kcat -C -b mybroker -t ais -p 2
% Reached end of topic ais [2] at offset 7959
```