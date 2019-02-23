# zabbix-barman

Barman monitoring template for Zabbix.

## Requirements

In order to work you need to configure following option for Zabbix 

* In your `sudoers` file add following option:
```sudoers
    zabbix ALL=(barman) NOPASSWD: /usr/bin/barman, /etc/zabbix/scripts/barman_discovery.py
```
* Copy the `userparameter_barman.conf` file to your zabbix agent on the barman server 

* Restart zabbix-agent

```sh
$ sudo systemctl restart zabbix-agent
```

* Import `Template Barman.xml` in the Zabbix Server

* Link Template to your Barman Server

* Auto Discovery will do the rest

