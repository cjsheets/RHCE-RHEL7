<h1>SE-Linux</h1>

Enforcing Options:

- `MAC`: Manditory access controls
- `DAC`: Discressionary access control
  - users, files, directories, memory, sockets, ports, etc.

2 Policies, defined in /etc/selinux/config (or run /usr/sbin/sestatus)

- Targeted - default, only processes with policy are confined
- MLS - multi-level security, everything is confined (TLA/mainly govornment)

##Labeling

Nearly everything in Linux is represented as a file. Every file, process, port in SELinux is defined
by a label either stored as extended attributes in the file system or managed by the kernel.

- Format: `user:role:type:level(optional)`
  - user, role and level are used in advanced configurations (MLS/MCS)

**Type Enforcement**
