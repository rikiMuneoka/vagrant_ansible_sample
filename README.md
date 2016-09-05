## Overview

Building simple lamp by vagrant with ansible.

## Requirement

* VirtualBox
* vagrant
* ansible

## Usage

```
$ mkdir sample_centos7
$ vagrant box add centos7 https://github.com/tommy-muehle/puppet-vagrant-boxes/releases/download/1.1.0/centos-7.0-x86_64.box
$ vagrant init -m
$ vagrant up
$ vagrant ssh
```
