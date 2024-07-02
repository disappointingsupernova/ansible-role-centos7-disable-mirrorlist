# ansible-role-centos7-disable-mirrorlist

An Ansible role that performs tasks related to CentOS 7 repositories:

- Checks if the operating system is CentOS 7.
- Creates a Vault repository file if the OS is CentOS 7.
- Finds existing CentOS repository files.
- Comments out the mirrorlist in repository files.
- Sets baseurl to `vault.centos.org` in repository files.

## Requirements

This role assumes you have Ansible installed and a basic understanding of how Ansible roles work.

## Role Variables

No specific variables are required for this role.

## Dependencies

None.

## Example Playbook

```yaml
- name: Apply Vault Repo for CentOS 7
  hosts: all
  become: yes
  roles:
    - centos7-vault
```