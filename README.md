K8SSETUP
=========

## Ansible role for setup Kubernetes Multi Node Cluster

- This repo will help you to setup the kubernetes cluster in AWS(Amazon Web Services)

#### AWS

- launch_aws.yml helps you to launch the ec2 instance in the cloud.
- Add the credentials of your aws account.
- To add more worker nodes add node name in the vars/main.yml file.

#### Kubernetes

- Setting up Multi Node Cluster is a big task.

#### Ansible

- With a single ansible-playbook, we can setup everything.


Requirements
------------

- Prefer to use AWS EC2 instances with Amazon Linux image. Use Kube_Master tag for EC2 instanceto setup the master node specifically. 
- You can also use RED-HAT image from AWS or other cloud providers.
- You should have basic knowledge on using Ansible roles
- Add access_key and secret_key in the vars/main.yml if you wish to launch the EC2 instances from ansible-playbook 


Role Variables
--------------

- Use the default vars/main.yml it contains all the information required to launch EC2 instances. If you want more worker nodes add names in the tags section.
- Also add secret keys to the vars/main.yml file.

Dependencies
------------

- There are no other role dependencies required to run the playbook.

Example Playbook
----------------

To run the palybook with the Kubernetes role.

    - hosts: servers
      roles:
         - k8ssetup

License
-------

BSD

Author Information
------------------

Technology enthusiast exploring the open source tools and contributing for simplifying the big tasks.
