# dokku-ports

Open and close your dokku app's ports.

Sometimes you just can't use the usual virtual host-based configuration of dokku, thus needing another way to access the ports used by your applications.
This plugin assumes two things:
* You are using [UFW](https://launchpad.net/ufw) to manage your firewall.
* You have already set up UFW on your server.

## Installation

    cd /var/lib/dokku/plugins
    sudo git clone git@github.com:heichblatt/dokku-ports.git
    sudo dokku plugins-install

## Usage

* Show all ports belonging to <app>

    ports <app>

* Close all ports belonging to <app>

    ports:close <app>

* Open all ports belonging to <app>

    ports:open <app> 
