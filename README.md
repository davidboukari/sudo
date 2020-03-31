# sudo

* https://www.tecmint.com/run-sudo-command-without-password-linux/

```bash
user_list host_list=effective_user_list tag_list comma
```

* user_list – list of users or a user alias that has already been set.
* host_list – list of hosts or a host alias on which users can run sudo.
* effective_user_list – list of users they must be running as or a run as alias.
* tag_list – list of tags such as NOPASSWD.
* command_list – list of commands or a command alias to be run by user(s) using sudo.

## Command to edit

```bash
visudo
```

## Set rights

```bash
# Add right for the user aaronkilik
aaronkilik ALL=(ALL) NOPASSWD: ALL
aaronkilik ALL=(ALL) NOPASSWD: /bin/kill

# Add right for the group sys
%sys ALL=(ALL) NOPASSWD: ALL
%sys ALL=(ALL) NOPASSWD: /bin/kill, /bin/rm
```

## Exec multiple commands

```bash
sudo -- bash -c 'apt-get update -y && apt-get install fail2ban -y
```
