Ansible role: PHP
=========

This role helps you to install php on your linux machine.


|Travis|GitHubActions|Quality|Downloads|Version|
|------|-------------|-------|---------|-------|
|[![travis](https://travis-ci.com/amine7777/ansible-role-php.svg?branch=master)](https://travis-ci.com/amine7777/ansible-role-php)|[![github](https://github.com/amine7777/ansible-role-php/workflows/CI/badge.svg)](https://github.com/amine7777/ansible-role-php/actions)|[![quality](https://img.shields.io/ansible/quality/50498)](https://galaxy.ansible.com/amine7777/php)|[![downloads](https://img.shields.io/ansible/role/d/50498)](https://galaxy.ansible.com/amine7777/php)|[![Version](https://img.shields.io/github/release/amine7777/ansible-role-php.svg)](https://github.com/amine7777/ansible-role-php/releases/)|

![](php.jpg)

Requirements
------------
- Linux machine
- Ansible 2.10

Role Variables
--------------
These variables helps to manage php installation.

You can specify your php version in this variable.
```yaml
php_version: php73
```
This is the url where php will be downloaded.
```yaml
php_download_url: 'https://releases.hashicorp.com/php/{{ php_version }}/php_{{ php_version }}_linux_{{ php_arch }}.zip'
```
This is the path where packer binary will be stored.
```yaml
php_directory_path: /usr/local/bin
```

Example Playbook
----------------

```yaml
- hosts: all
  roles:
     - amine7777.php
```


Author Information
------------------

- [Amine Kahlaoui](https://github.com/amine7777), DevOps engineer.
