# Ansible Role: SNMP

[![Build Status](https://travis-ci.org/sbaerlocher/ansible.snmp.svg?branch=master)](https://travis-ci.org/sbaerlocher/ansible.snmp)

## Description

Ansible role for installing and Configuration SNMP v3 on installs RHEL/CentOS or Debian/Ubuntu.

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

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.snmp
```

## Changelog

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

(c) 2017, Simon Bärlocher
