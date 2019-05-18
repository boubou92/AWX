# Project Title

Install AWX with prerequise.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.


### Prerequisites

You must have sudo user on the machine where AWX will be installed.
If you have two server
- Ansible controler
- remote server

Create key on your ansible controller :

```
sshkeygen -t rsa
```

```
ssh-copy-id sudouser@remoteserver
```

Test your ssh connection by login to remote server:
```
ssh sudouser@remoteserver
```
I you are install AWX on localhost you need have already installed
- git
- ansible
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#latest-releases-via-apt-ubuntu

If you want install AWX on remote server, playbook will install all package, included git and ansible

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


