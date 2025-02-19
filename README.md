![ci](https://github.com/rafael-c-alexandre/ansible-role-ntp/actions/workflows/ci.yml/badge.svg)
![release](https://github.com/rafael-c-alexandre/ansible-role-ntp/actions/workflows/release.yml/badge.svg)

rafael-c-alexandre.ntp
=========

An Ansible role to configure the NTP (Network Time Protocol) service and set the system timezone on Debian servers.

**Note:** For now, only `systemd-timesyncd` package is supported as the NTP service. There are plans to extend support to other services such as chrony.

Requirements
------------

- **Ansible Version**: Ensure you are running Ansible version 2.18 or higher.
- **Supported Systems**: This role is designed for Debian-based systems.

Role Variables
--------------

The following variable can be customized to configure the role. The default value is defined in `defaults/main.yml`.

- `ntp_timezone`: *(Default: `"Europe/Amsterdam"`)* The timezone to set on the target system.


Dependencies
------------

This role has no external dependencies.

Example Playbook
----------------

```yaml
- hosts: all
  become: true
  roles:
    - role: rafael-c-alexandre.ntp
      vars:
        ntp_timezone: "America/New_York"
```

License
-------

MIT
