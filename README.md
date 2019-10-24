# Ansible Role: SNMP

[![Build Status](https://img.shields.io/travis/sbaerlocher/ansible.snmp.svg?branch=master&style=popout-square)](https://travis-ci.org/sbaerlocher/ansible.snmp) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-snmp-blue.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/snmp) [![Ansible Role](https://img.shields.io/ansible/role/d/9234.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/snmp)

## Description

Ansible role for installing and Configuration SNMP v3 on installs RHEL/CentOS or Debian/Ubuntu and SNMP v2 on Windows.

## Installation

```bash
ansible-galaxy install sbaerlocher.snmp
```

## Requirements

## Role Variables

| Variable             | Default         | Comments (type)                                   |
| :---                 | :---            | :---                                              |
| snmp_user            | snmp            | SNMP User                                         |
| snmp_password        | snmp_password   | SNMP Password                                     |
| snmp_encryption      | snmp_encryption | SNMP Encryption                                   |
| snmp_contact         |                 | Optional: System Contact                          |
| snmp_location        |                 | Optional: System Location                         |
| snmp_agentaddress_protocol.ipvX | udp / udp6 | Optional: SNMP Protocol, X for ipv4 or ipv6
| snmp_agentaddress_address.ipvX | {{ ansible_default_ipv4.address }} / {{ ansible_default_ipv6.address }} |  Optional: SNMP bind address, X for ipv4 or ipv6 |
| snmp_agentaddress_port.ipvX | 161 / 161 | Optional: SNMP port, X for ipv4 or ipv6 |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.snmp
```

## Changelog

### 1.7.1

* add support for Windows 1809

### 1.7.0

* add osupdate support
* syntax cleaned up

### 1.6.0

* add distro support
* syntax cleaned up
* proxmox support

### 1.5

* add Windows Support

### 1.4

* add IP bind support

### 1.3

* add become support
* new role check
* support for sysContact and sysLocation

### 1.2

* add package manager for generic OS
* cleanup

### 1.1

* add ArchLinux support

### 1.0

* Initial release

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2018, Simon Bärlocher
