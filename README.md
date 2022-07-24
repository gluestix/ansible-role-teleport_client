# Ansible Role: Teleport Client

[![CI](https://github.com/gluestix/ansible-role-teleport-client/actions/workflows/ci.yml/badge.svg)](https://github.com/gluestix/ansible-role-teleport-client/actions/workflows/ci.yml) [![KICS](https://github.com/gluestix/ansible-role-teleport_client/actions/workflows/kics.yml/badge.svg)](https://github.com/gluestix/ansible-role-teleport_client/actions/workflows/kics.yml)

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
teleport_version: "10.0.2-1"
```

The version of Teleport to install, supports `latest`. I recommend only setting this to `latest` in the event that you are managing which version of Teleport is available with some kind of life cycle management (i.e. with Red Hat Satellite) as you wouldn't want to push a versionf Teleport broken.

```yaml
teleport_auth_token: ""
teleport_ca_pin: ""
teleport_auth_servers:
  - "155.33.137.15"
```

Settings to authenicate with the Teleport auth server using.

```yaml
teleport_listen_port: "3022"
```

Port teleport will listen on.

```yaml
teleport_labels_environment: "dev"
teleport_labels_team: "it"
```

What labels the host will have.

```
teleport_x11_enabled: false
```

Wether x11 forwarding is allowed.

