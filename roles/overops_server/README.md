OverOps Backend Server
=========

This role installs the OverOps Backend (Analysis) Server for On-Premises installations.

Requirements
------------
Prerequisites for the OverOps Backend Server can be found here:
* https://doc.overops.com/docs/overops-installation-requirements#section-overops-server-on-premises-installation-requirements


The role is based OverOps install procedures found here:
* https://doc.overops.com/docs/on-premises-installation
* https://doc.overops.com/docs/install-analysis-server



Role Variables
--------------

The role variables are base on the installation options described on the following doc site:
* https://doc.overops.com/docs/on-premises-advanced-command-line-non-docker

The following variables are specific to the ansible role:

    installation_dir: '/opt/takipi-server'

Installation Directory where server will be installed into.

    installer_location: 'https://s3.amazonaws.com/app-takipi-com/deploy/takipi-server/takipi-server-java.tar.gz'

URL or target folder path where the installer is located.

    installer_is_remote: true

Flag to indicate that the installer is a remote URL or local file on the target server.

    install_drivers: true

Flag to indicate that the Database driver should also be downloaded and installed.

    ojdbc_driver_url:

URL where OJDBC Driver is located.

    mysql_driver_url:

URL where MYSQL Driver is located.


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
    - overops_server
  vars:
    daemon_user: 'overops'
    daemon_group: 'overops'
```
License
-------

Apache 2.0