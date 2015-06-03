Ansible - Hostname
=========

Configure system hostname and update hosts files.

Requirements
------------------

The hostname is determined from the FQDN in your inventory file.

```ini
[servers]
server-a.example.com     ansible_ssh_host=10.0.0.1
server-b.example.com     ansible_ssh_host=10.0.0.2
```

In this example, the hostname will be set to server-a and server-b (aka: ```{{ inventory_hostname_short }}``` ) respectively.
The local hosts file will also be updated to resolve the short and fully qualified versions for both IPv4 and IPv6

Usage
----------------

```yaml
  - hosts: all
    roles:
      - { role: elliot.hostname }
```

TODO
------------------

  - [ ] Add support for RHEL based systems

License
------------------

This project is licensed under the MIT license.

Author Information
------------------

Elliot Anderson ([Email](mailto:elliot.a@gmail.com), [Twitter](http://www.twitter.com/elliotanderson))
