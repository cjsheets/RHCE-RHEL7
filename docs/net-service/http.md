<h1>Network Services :: HTTP</h1>

Apache is the default http server

## Install

`yum install httpd`

## Manage Service

```
systemctl enable httpd

systemctl start httpd
```

## Defaults

* `/var/www/html` - default web directory

* `/etc/httpd/conf/httpd.conf` - default configuration

## Security

**Open Firewall on Port 80**

`firewall-cmd --permanent --add-service=http`

`firewall-cmd --reload`

**Apply SELinux Context**

`chcon -R --reference=/var/www/html /var/www/html/dvd`

* `-R` - recursively
* `--reference=` - apply the context taken from the ref directory