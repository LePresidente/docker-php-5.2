# Docker image for php 5.2 legacy projects
This docker image is intended to work as a replacement for old legacy projects, running on old server.
The features are
* Based on Ubuntu 12.04
* Apache MPM Prefork
* PHP 5.2.17 as apache mod
* Zend Optimizer (disabled for xdebug)

Features added by apelliciari:
* Xdebug 2.2.7
* enabled short tag PHP

NOTE: To enable mailing, you need to configure ssmtp. This can be done by adding a file `ADD ssmtp.conf /etc/ssmtp/` containing a config like this
```
# See https://linux.die.net/man/5/ssmtp.conf
Mailhub=<Server>
AuthUser=<User>
AuthPass=<Pass>
Hostname=<Senders Host>
FromLineOverride=YES
UseTLS=YES
UseSTARTTLS=YES
```
