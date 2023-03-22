# ansible-software.install
Ansible-playbook to install some packages to your Linux server.

## packages
* Docker CE
* nginx
* MariaDB 10.10
* PHP
    * php-cli
    * php-curl
    * php-fpm
    * php-gd
    * php-imap
    * php-mbstring
    * php-mysql
    * php-soap
    * php-xml
    * php-zip
* certbot

## requirments
* Debian, Ubuntu
* Ansible >= 2.9.6
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
* Uncomment required software in file **`software-install.yaml`**
* Change PHP version if you need it

## using
```Bash
ansible-playbook software-install.yaml -e "hosts=YOUR-HOST-NAME"
```
