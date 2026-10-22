# Phansible Role: Composer

[![CI](https://github.com/phansible/role-composer/actions/workflows/ci.yml/badge.svg)](https://github.com/phansible/role-composer/actions/workflows/ci.yml)

An Ansible Role that installs [Composer](https://getcomposer.org/), the PHP Dependency Manager, with the official installer after checking its published SHA-384 signature, specifically created with [Phansible](http://phansible.com/) in mind.

## Requirements

- Ubuntu 22.04, 24.04, 26.04 or Debian 12, 13
- Ansible >= 2.15
- PHP CLI installed earlier in the play, for example by [role-php](https://github.com/phansible/role-php)

## Role Variables

None. Composer is installed to `/usr/local/bin/composer` and left alone once it exists; run `composer self-update` to upgrade it.

## Dependencies

[role-php](https://github.com/phansible/role-php), listed before this role in the play.

## Example Playbook

```yaml
- hosts: all
  become: yes
  roles:
    - role-php
    - role-composer
```

## License

This role is released under the terms of the license specified in the repository or if not specified, under the [MIT license](https://raw.githubusercontent.com/phansible/role-composer/master/LICENSE).

## Author Information

This role was created in 2015 by [The Phansible Team & Contributors](https://github.com/phansible/role-composer/graphs/contributors), credits go also to [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/) and source of inspiration.
