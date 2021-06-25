# ansible-software.install
Ansible-playbook to install some packages to your Linux server.

## packages
* nginx
* MariaDB 10.5
* PHP8.0
    * php8.0-fpm
    * php8.0-gd
    * php8.0-xml
    * php8.0-soap
    * php8.0-mbstring
    * php8.0-mysql
    * php8.0-imap
    * php8.0-curl
    * php8.0-zip
* certbot

## requirments
* Debian, Ubuntu, CentOS7/8
* Ansible <= 2.9.6
* ansible-collection [community.general](https://github.com/ansible-collections/community.general)

## installing
1. Clone project from GitHub repository
```bash
git clone https://github.com/vargaloid/ansible-software.install.git
```
2. Install collection community.general
```bash
ansible-galaxy collection install community.general
```

## configuring
Just uncomment required software in file **`software-install.yml`**

## using
```Bash
ansible-playbook software-install.yml -e "hosts=YOUR-HOST-NAME"
```
