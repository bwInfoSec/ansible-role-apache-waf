[![Molecule Test](https://github.com/bwInfoSec/ansible-role-apache-waf/actions/workflows/molecule-test.yml/badge.svg)](https://github.com/bwInfoSec/ansible-role-apache-waf/actions/workflows/molecule-test.yml)

ansible-role-apache-waf
=========

Install and configure apache2 with mod-security paranoia level 1. This should work for almost all usecases without adaption.

## Platforms

- RHEL 8
- RHEL 7
- Debian 10
- Debian 11
- Ubuntu 18.04
- Ubuntu 20.04
- Ubuntu 22.04

## Install

``` sh
ansible-galaxy install bwinfosec.apache_waf
```

## Example Playbook

```yml
- name: Setup webserver with WAF
  hosts: webserver
  become: true

  roles:
    - bwinfosec.apache_waf
```

## Local Development
This role includes a *Molecule* test to execute on RHEL/CentOS, Debian and Ubuntu.

To run all scenarios (i.e. test all platforms):

```bash
$ molecule test --all
```

To run a specific scenario by name:

```bash
$ molecule test --scenario-name ubuntu
$ molecule test --scenario-name debian
$ molecule test --scenario-name centos
```

## Licensing
This work is licensed under the [LGPL](https://www.gnu.org/licenses/lgpl-3.0.html) AND the [EUPL 1.2](https://joinup.ec.europa.eu/collection/eupl/eupl-text-eupl-12).

If you redistribute this code please also include the AUTHORS file.

## Contribution
If you want to contribute feel free to do so by creating a pull request on [github](https://github.com/bwInfoSec/ansible-role-apache-waf).
