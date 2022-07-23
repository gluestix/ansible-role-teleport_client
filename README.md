[![CI](https://github.com/gluestix/ansible-role-teleport-client/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/gluestix/ansible-role-teleport-client/actions/workflows/ci.yml)
# Ansible Role: Teleport Client

An Ansible role that installs and configures [Teleport](https://goteleport.com/) SSH server access on EL 8.

## Requirements

A Teleport authentication server and the proper authencation credentials.

## Role Variables

Available variables are listed, below, along with default values (see `defaults/main.yml`):

```yaml
teleport_config_firewall: true
```

Whether or not to configure the system firewall open the Teleport SSH server port to only the auth server. If you have a seperate application managing firewall rules then this should be disabled.

```yaml
teleport_version: "10.0.0-1"
```



The version of Teleport to install, supports `latest`.

```yaml
teleport_auth_token: ""
teleport_ca_pin: ""
teleport_auth_servers:
  - "0.0.0.0"
```

Settings to authenicate with the Teleport auth server.





