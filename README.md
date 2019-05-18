# Project Title

Install AWX with prerequise.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.


### Prerequisites

Of course you must have git installed on your machine, if it's not the case the package will be installed by roles prerequis_install
you must install:

```
 Ansible
```
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#latest-releases-via-apt-ubuntu

This project have been done for ubuntu 18.04 bionic, but you can use it for another version. please change whith yout correct version
the variable

- "{{docker_repo}}"

located in

```
/roles/prerequis_install/vars/main.yml

```

### Installing

Go in project folder and run command: 

```
ansible-playbook -i hosts master_playbook.yml 
```
- The first role is installation of prerequise 
- The second role is installation of AWX

## hosts file

hosts file is only include localhost, please change or add your hosts in this file.

### master_playbook

This entry of playbook, it will list all roles and hosts



## Connect to AWX GUI

go to http://127.0.0.1 or DNS name of your server 
- login: admin
- password: password



## Authors

* **Rabah Bourahla** 


## License

no licence

## Acknowledgments

https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#latest-releases-via-apt-ubuntu
https://github.com/ansible/awx/blob/devel/INSTALL.md
https://github.com/ansible/awx


