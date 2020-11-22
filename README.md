Ansible role: PHP
=========

This role helps you to install php on your linux machine.


|Travis|GitHubActions|Quality|Downloads|Version|
|------|-------------|-------|---------|-------|
|[![travis](https://travis-ci.com/amine7777/ansible-role-php.svg?branch=master)](https://travis-ci.com/amine7777/ansible-role-php)|[![github](https://github.com/amine7777/ansible-role-php/workflows/CI/badge.svg)](https://github.com/amine7777/ansible-role-php/actions)|[![quality](https://img.shields.io/ansible/quality/51931)](https://galaxy.ansible.com/amine7777/php)|[![downloads](https://img.shields.io/ansible/role/d/51931)](https://galaxy.ansible.com/amine7777/php)|[![Version](https://img.shields.io/github/release/amine7777/ansible-role-php.svg)](https://github.com/amine7777/ansible-role-php/releases/)|


<img src="php.png" alt="ansible hosts" width="500"/>


Requirements
------------
- Linux machine
- Ansible 2.10

Role Variables
--------------
These variables helps to manage php installation.

You can specify your php version in these 2 variables. For example if you would like to install php73, the values will be the following:
```yaml
php_major_version: 7
php_minor_version: 3
```
Php is installed using [Remi's RPM repository](https://blog.remirepo.net/) for Centos and Fedora. 

If you would like to install more php packages you need to create a list using php packages lis.

For Centos and Fedora: php73-<package_name>
```yaml
php_packages:
  - php73-mysql
```

For Ubuntu and Debian: php7.3-<package_name>
```yaml
php_packages:
  - php7.3-mysql
```

Example Playbook
----------------

```yaml
- hosts: all
  vars:
    php_major_version: 7
    php_minor_version: 4
  roles:
     - amine7777.php
```


Author Information
------------------

- [Amine Kahlaoui](https://github.com/amine7777), DevOps engineer.
