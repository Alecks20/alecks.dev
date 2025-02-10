
+++
author = "Alecks"
title = "Securing your Linux servers ssh."
date = "2024-04-25"
description = "Guide to emoji usage in Hugo"
tags = [
    "linux","servers","ssh","security"
]
+++

This post is made for debian based linux distros, most won't work on other distros

## Non-root account for logins
When securing ssh on your server the first thing you want to to do is change the user you login as, start with making a new user with any username you want

```
adduser declan
```

After that add it to the list of sudoers

```
usermod -aG sudo declan
```

## Moving to SSH keys
I think it should be pretty obvious that using plaintext passwords for logging into your system isn't the best idea, so thats why you should use something like PuTTYGen to generate an ssh key, generate a new key then copy and paste the public key generated into `/home/declan/.ssh/authorized_keys` (Change to your username)

Each key is seperated by a new line, simply paste the key in with no spaces or anything else around

## Changing the SSH configuration
This process can differ depending on your host, but for most servers the ssh config is located in `/etc/ssh/sshd_config.d`, in this file you want to change the following values

```
PubkeyAuthentication yes
```

```
PasswordAuthentication no
```

```
PermitRootLogin no
```

```
Port 13923
```

This will disable password authentication, disable root login (Make sure you've setup another account) and allow you to login using ssh keys, which I showed how to setup above and change the ssh port

Run the command below to apply the ssh configuration settings

```
sudo systemctl restart ssh
```

## Configuring a firewall
You can use UFW which is preinstalled on ubuntu and can be installed on debian using apt, it can be easily setup using a few commands, a firewall blocks connections to ports or services you don't want exposed

### Allowing/Denying a port

```
ufw allow [port]
```

```
ufw deny [port]
```

### Allowing a range of ports

```
ufw allow [port]:[port]/tcp
```

```
ufw allow [port]:[port]/udp
```

### Enabling the firewall

```
ufw enable
```

### Checking firewall status

```
ufw status
```

## NTFY notifcations on login
As an extra security precaution you can use ntfy to get mobile notifications whenever someone remotely connects to your server, I used [this](https://paramdeo.com/blog/enabling-ssh-login-notifications-using-ntfy) tutorial and it worked for me, you can also find an example on the ntfy docs [here](https://docs.ntfy.sh/examples/#ssh-login-alerts)