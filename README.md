# mablanco.tiger

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
