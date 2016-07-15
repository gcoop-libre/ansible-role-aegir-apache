Aegir Apache
============

Extends the gcoop-libre.apache role to allow usage as an Aegir remote server.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    aegir_apache_sudoers_file: /etc/sudoers

The path of the sudoers file where the Aegir system user will be added, so it can restart Apache after changing the VHosts.

    aegir_apache_user_in_apache_group: True

This property will add the Aegir system user to the Apache system group.

Dependencies
------------

- `opendevshop.aegir-user`
- `geerlingguy.git`
- `gcoop-libre.apache`

Example Playbook
----------------

    - hosts: hostmasters
      roles:
         - gcoop-libre.aegir-apache

License
-------

GPLv2

Author Information
------------------

This role was created in 2016 by [gcoop Cooperativa de Software Libre](http://gcoop.coop).

This role is a fork of the role created by [OpenDevShop](https://github.com/opendevshop).
