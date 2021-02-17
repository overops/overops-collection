OverOps Collector
=========

This role installs the OverOps Collector software

Requirements
------------
Prerequisites for the OverOps Backend Server can be found here:
* https://doc.overops.com/docs/overops-installation-requirements#section-collector-system-requirements


The role is based OverOps install procedures found here:
* https://doc.overops.com/docs/install-a-collector-on-linux


Role Variables
--------------

The role variables are base on the installation options described on the following doc site:
* https://doc.overops.com/docs/collector-properties
* Encryption: https://doc.overops.com/docs/encryption-between-overops-components

The following variables are specific to the ansible role:

    installation_key: ''

Required: Installation Key provided to connect to OverOps SaSS or Backend.

    installation_dir: '/opt/takipi'

Installation Directory where server will be installed into.

    installer_location: 'https://app.overops.com/app/download?t=tgz'

URL or target folder path where the installer is located.

    installer_is_remote: true

Flag to indicate that the installer is a remote URL or local file on the target server.

    enable_service: true

Flag to indicate that the collector should install as systemd service.


Dependencies
------------

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
---
- hosts: localhost
  collections:
    - overops.overops_collection

  roles:
    - collector
  vars:
    installation_key: "YOUR_KEY"
```
License
-------

Apache 2.0