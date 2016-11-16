# WordPress Ansible Ubuntu 16.04 Nginx

This repo contains a playbook for provisioning WordPress on Ubuntu 16.04. 


The following is handled out of the box:

* User setup
* SSH hardening
* Firewall setup
* Nginx with HTTP/2 (with improved default configs)
* PHP 7
* MariaDB
* Redis
* WP-CLI
* Fail2Ban
* Git

## Usage

Configure `/hosts` file.

```
[production]
192.168.1.1 #sampledomain.com
```

Edit `/provision.yml` to configure default user - http://docs.ansible.com/ansible/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module sudo password and local public key path. 

Run:

`ansible-playbook provision.yml`