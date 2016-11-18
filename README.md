# Personal playbook

This is my personal [Ansible](https://www.ansible.com/) playbook to set up a freshly installed [Ubuntu](https://www.ubuntu.com/) with the softwares I prefer to use.

## Setup

First Ansible needs to be installed:
```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

## Run it

After installing Ansible and cloning this repo you can run the playbook to execute all tasks:
```
$ ansible-playbook -K -i inventory playbook.yml
```

Or just a tagged task, e.g. install atom text editor:
```
$ ansible-playbook -K -i inventory playbook.yml --tags atom
```

Note: you can turn off cowsay via:
```
$ export ANSIBLE_NOCOWS=1
```
