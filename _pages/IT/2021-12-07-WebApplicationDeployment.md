---
title: ""  
excerpt: ""  
categories:
- 
tags:
- 

Requirement:
1. A server hosting your application (Cloud services) -digital ocean, linode
2. Server (provisioned) & Operating System (installed)
3. Web Servers & WSGI Servers 
 Web Server Gateway Interface (standard interface btw the built & the one executing(running)) 
4. Application Dependencies
5. Automation with Ansible (a configuration management tool, built in Python)
---

Steps
1. Create a digitalocean account
  - size: 10/m
  - datacenter: close to your customers

  -Add your SSH keys:
    -go to Ubuntu and create an ssh key
      > ssh-keygen -t rsa -b 2048
    -save it under a directory(/home/simon/do_deploy)
    -two files (private/public keys) generated
    -no passphrase
    -check the public key by
      > cat /home/simon/do_deploy.pub
    -paste it to New SSH Key (DigitalOcean)
  - Create a Single Droplet
  - Give a host name
  - Copy IP Address
  - Connect to the server as *root*
    > ssh -i /home/simon/do_deploy root@**ip address** 
    ('i' is used to specify a particular private key)
    >
 Ansible
  - Configuration management tool
  - Written in Python
  - Pip install ansible
  - python 3 compatible (check)
  - Module-based system
  - Playbooks 
    - initial configuration for lockdown the system (run single time)
    - every deployment
  - Tasks
  - Yet Another Markup Language (YAML)
  - Refer to doc(module index) while writing the playbook: