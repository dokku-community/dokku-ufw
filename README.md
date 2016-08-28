# dokku-ports [![Build Status](https://img.shields.io/travis/heichblatt/dokku-ports.svg?branch=master "Build Status")](https://travis-ci.org/heichblatt/dokku-ports)

Open and close your dokku app's ports.

Sometimes you just can't use the usual virtual host-based configuration of dokku, thus needing another way to access the ports used by your applications.
This plugin assumes two things:

* You are using [UFW](https://launchpad.net/ufw) to manage your firewall.
* You have already set up UFW on your server.

## requirements

- dokku 0.4.0+
- docker 1.8.x

## installation

```shell
# on 0.3.x
cd /var/lib/dokku/plugins
git clone https://github.com/heichblatt/dokku-ports.git ports
dokku plugins-install

# on 0.4.x
dokku plugin:install https://github.com/heichblatt/dokku-ports.git ports
```

## hooks

This plugin provides hooks:

* `post-deploy`: open ports for app
* `pre-delete`: close ports for app

## usage

```shell
# Show all ports belonging to app
dokku ports <app>

# Close all ports belonging to app
ports:close <app>

# Open all ports belonging to app
ports:open <app>
```
