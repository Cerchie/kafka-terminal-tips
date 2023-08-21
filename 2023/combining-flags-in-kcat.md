When you're using kcat https://github.com/edenhill/kcat, it can be helpful to shorten your commands
by combining single-letter flags.

For example, to consume from topic `topicname` in consumer mode, you could enter the 
`t` and `C` flags separately like this:

```
kcat -t topicname -C    
```
Or combine them like this: 

```
kcat -Ct topicname    
```