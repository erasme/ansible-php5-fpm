php5-fpm Ansible playbook
=========================

[![Travis
CI](http://img.shields.io/travis/erasme/ansible-php5-fpm.svg?style=flat)](http://travis-ci.org/erasme/ansible-php5-fpm)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansible--php5--fpm-blue.svg?style=flat)](https://github.com/erasme/ansible-roles-specs/tree/master/ansible-php5-fpm/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-erasme.php5--fpm-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2971)

This playbook will install php5-fpm.

Requirements
------------

Required packages (installed automatically) :

  - php5-fpm
  - php-apc
  - php5-mcrypt
  - php5-gd
  - php5-curl
  - php-pear
  - php5-mysql

Role Variables
--------------

  - `php5_post_max_size`: max post size (default: 40M)
  - `php5_upload_max_filesize`: max upload size for files (default: 20M)
  - `php5_add_nginx_default`: whether the role will add a default & php5-fpm-enabled virtuahost in nginx config


Tags
----

  - `php5-fpm` : applies to the whole role

Dependencies
------------

  - erasme.nginx

Example Playbook
----------------

This is mainly used as a dependency in your existing playbooks, like:

    dependencies:
      - { role: erasme.php5-fpm }

but can be used in playbooks also :

  - name: web servers
    hosts: webservers
    roles:
      - php5-fpm

License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

