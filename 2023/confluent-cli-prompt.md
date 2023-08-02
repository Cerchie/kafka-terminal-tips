USED 08-02-23

You can add info from the `confluent` cli to your terminal prompt. First, set up your `~/bashrc`

```
export PS1='$(confluent prompt) '$PS1
```

or ~.zshrc

```
setopt prompt_subst
export PS1='$(confluent prompt) '$PS1
```

Then, try running 

```
confluent prompt -f %a
```

to see your current API key! To view other formatting tokens, visit our [docs page on the `confluent prompt` command.](https://docs.confluent.io/confluent-cli/current/command-reference/confluent_prompt.html#confluent-prompt) 
