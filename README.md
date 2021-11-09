# Udemy Ansible Assignment

This is a solution for the Ansible Assignment on Udemy https://www.udemy.com/learn-ansible-advanced

This assignment tests the students knowledge on deploying a distributed web application on cloud using fully automated Ansible playbooks. The solution is shared to the instructor and student community using github repository and feedback will be given.

**A full video demonstration of the solution is under development. Will update once ready.**

## Solution
Below is my solution to the problem. 

### Infrastructure 
 
I chose aws cloud as development environment.

### Development Environment

I spun up multiple instances to for ansible controller and targets so that  I can  proceeded to develop my project and test.

### Ansible Project

I decided to use tasks file for deploying instances and create my own roles to configure those instances with Application.
​       
- **Tasks:** A role to deploy necessary compute instances on on AWS Cloud
- **Roles:** ansible-role-mysql: A role to install and configure MySQL on any given systems
- **Roles:** ansible-role-flask-web: A role to install and configure Flask application on multiple 
- **Tasks:** Configure native AWS Load Balancing and Security group
- **Tasks:** Send email notification

Group Variables to have following properties:


- **db_name:** Database name
- **db_user:** Database user to create
- **db_password:** Password for the Database user
- **machine_type:** Type of machine to deploy eg: n1-standard-1  
​- **image:** Image of instance to deploy debian-7
- **db_name:** Database name
- **db_user:** Database user
- **db_user_password:** Database user password
- **ansible_user:** User to connect to Compute Instances using gcloud compute ssh
- **ansible_ssh_private_key_file:** Private key file to connect to Compute Instances using gcloud compute ssh
