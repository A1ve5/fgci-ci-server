This is pretty much a "Work in Progress" project.

Deploy Jenkins on CSC Cloud Computing Platform
==============================================

This playbook should allow you to deploy and configure a Jenkins server on CSC Cloud Computing Platform (Pouta) and is based on:

  - https://github.com/CSC-IT-Center-for-Science/pouta-ansible-demo.git
  - https://github.com/ICTO/ansible-jenkins role


# Requirements

Get ansible-jenkins role:

```bash
$ git clone https://github.com/ICTO/ansible-jenkins.git roles
```

## pouta-ansible-demo Requirements

Simple Ansible demo to deploy a machine to Pouta 

To use this demo you will need:
 - Ansible 2.0: http://docs.ansible.com/intro_installation.html
 - Python >=2.7: Needed by the os_security_group ansible module
 - OpenStack command line tools: http://docs.openstack.org/user-guide/content/install_clients.html
 - Shade: pip install shade - http://docs.openstack.org/infra/shade/
 - Access to pouta: https://research.csc.fi/pouta-access
 - Your Pouta openstack RC file: https://research.csc.fi/pouta-install-client
 - Your SSH public key uploaded to Pouta: https://pouta.csc.fi/dashboard/project/access_and_security/

## Configuration:

See:
  - https://github.com/CSC-IT-Center-for-Science/pouta-ansible-demo.git
  - https://github.com/ICTO/ansible-jenkins

# To-Dos and Kown Issues:

 - ansible-jenkins role doesn't work for CentOS7 out-of-the-box. "chkconfig jenkins on" shell task needs to be replaced by "systemctl enable jenkins". A pull request is being prepared.
 - dynamic inventory
 - Server security hardening
