```
❯ st2 pack register example
+--------------+-------+
| Property     | Value |
+--------------+-------+
| actions      | 1     |
| aliases      | 0     |
| configs      | 0     |
| policies     | 0     |
| policy_types | 3     |
| rule_types   | 2     |
| rules        | 0     |
| runners      | 14    |
| sensors      | 0     |
| triggers     | 0     |
+--------------+-------+
```

```
❯ st2 pack register example
+--------------+-------+
| Property     | Value |
+--------------+-------+
| actions      | 1     |
| aliases      | 0     |
| configs      | 0     |
| policies     | 0     |
| policy_types | 3     |
| rule_types   | 2     |
| rules        | 0     |
| runners      | 14    |
| sensors      | 0     |
| triggers     | 0     |
+--------------+-------+
```

```
❯ st2 pack config example -y
password (secret): ******************
---
Do you want to preview the config in an editor before saving? [y]: n
---
Do you want me to save it? [y]: y
id: 637dbdac9f088118bd340c47
pack: example
values:
    password: '********'

❯ docker-compose exec st2client bash
Welcome to StackStorm HA v3.7.0 (Ubuntu 20.04.4 LTS GNU/Linux x86_64)
 * Documentation: https://docs.stackstorm.com/
 * Community: https://stackstorm.com/community-signup
 * Forum: https://forum.stackstorm.com/

 Here you can use StackStorm CLI. Examples:
   st2 action list --pack=core
   st2 run core.local cmd=date
   st2 run core.local_sudo cmd='apt-get update' --tail
   st2 execution list


root@01e2a3d1ffa6:/opt/stackstorm# cat configs/example.yaml
password: This is a password
```

```
❯ st2 run example.run_shell_script
.
id: 637dc1839f088118bd340c59
action.ref: example.run_shell_script
context.user: st2admin
parameters:
  password: '********'
status: succeeded
start_timestamp: Wed, 23 Nov 2022 06:45:23 UTC
end_timestamp: Wed, 23 Nov 2022 06:45:23 UTC
result:
  failed: false
  return_code: 0
  stderr: ''
  stdout: 'This is a default message
    This is a password'
  succeeded: true
```
