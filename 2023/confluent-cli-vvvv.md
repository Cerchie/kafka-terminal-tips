The Confluent CLI supports getting verbose information from commands. With every `v` you add, you get a different output! 

Here's an example. Say I'm having logging in and want to see any warnings: 

```
❯ confluent login -v
2023-06-07T13:48:02.180-0700 [WARN]  unable to read directory from `$PATH`: /Users/username/confluent-7.2.2/bin
Logged in as "username@email.com" for organization "hash" ("Org_Name").
```

I could get the output as just info by running the same command with `-vv`:

```
❯ confluent login -vv
Logged in as "username@email.com" for organization "hash" ("Org_Name").
```

Or, adding another `v`, I could see debug logs:

```
❯ confluent login -vvv
2023-06-07T13:50:51.282-0700 [DEBUG] Searching `$PATH` for plugins. Plugins can be disabled in /Users/username/.confluent/config.json.

2023-06-07T13:50:51.282-0700 [DEBUG] Did not find full credential set from environment variables
2023-06-07T13:50:51.293-0700 [DEBUG] Searching for netrc machine with filter: {IgnoreCert:false IsCloud:true Name:login-username@email.com-https://confluent.cloud URL:https://confluent.cloud}
...etc
```

With four `v`s, I get the trace stack, which has the same output as the above for many lines but is finer-grained:

```
❯ confluent login -vvvv
```