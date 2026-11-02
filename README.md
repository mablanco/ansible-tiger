# mablanco.tiger

> **DEPRECATED:** this role is no longer maintained and will not receive updates. Tiger itself has had no upstream development for many years, although Debian and Ubuntu still package it. Alternatives:
>
> - [Lynis](https://cisofy.com/lynis/), an actively maintained security auditing tool, deployed with the [`mablanco.lynis`](https://github.com/mablanco/ansible-lynis) role.
> - Tiger from your distribution's packages, with a single `ansible.builtin.package` task (`name: tiger`).

Ansible role to deploy Tiger, an open source security auditing tool, from the official Linux packages. If you want to receive the output of the default scheduled runs, you need to fill in the following variables.

Only Debian and Ubuntu are supported, right now.

## Role Variables

- **tiger_mail_from**: Sender email address for the audit report. No valid default, you have to fill it in.
- **tiger_mail_rcpt**: Receiver email address for the audit report. No valid default, you have to fill it in.

## Example Playbook

Example of how to use this role:

    - hosts: debian_servers
      vars:
         tiger_mail_from: 'sender@example.com'
         tiger_mail_rcpt: 'receiver@example.com'
      roles:
         - { role: mablanco.tiger }

## License

GPLv3
