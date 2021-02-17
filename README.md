# Ansible Collection - overops.overops_collection

Repo containing various ansible roles for installing OverOps Components.

## Installation

To install the collection with the `ansible-galaxy` command:

```
$ ansible-galaxy collection install overops.overops_collection

or form an archive:

$ ansible-galaxy collection install overops-overops_collection-1.0.0.tar.gz -p ./collections

```

## Example usage

Each role contains a readme that explains the use of the role and variables within. In order to use any role within the installed collection make sure to include the `overops.overops_collection` in the collections section in the playbook:

```yaml
---
- hosts: localhost
  collections:
    - overops.overops_collection

  roles:
    - overops_server
  vars:
    daemon_user: 'overops'
    daemon_group: 'overops'
```
