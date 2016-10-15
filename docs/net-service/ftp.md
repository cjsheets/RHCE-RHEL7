<h1>Network Services :: FTP</h1>

## Basic Configuration

- Verify contents exist in correct directory
- Verify contents configured with correct SELinux context
- Configure service to point to directory and start on boot

## Install

`yum install vsftpd`

## Manage Service

```
systemctl enable vsftpd

systemctl start vsftpd
```

## Defaults

* `/var/ftp/pub` - default ftp directory

* `/etc/vsftpd/vsftpd.conf` - default configuration

## Security

**Open Firewall on Port 21**

`firewall-cmd --permanent --add-service=ftp`

`firewall-cmd --reload`