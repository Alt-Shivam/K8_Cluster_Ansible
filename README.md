# K8_Cluster_Ansible
Deploy Kubernetes cluster using ansible playbooks


## Prerequisites
* An SSH key pair on your local Linux/macOS/BSD machine. If you haven’t used SSH keys before, you can learn how to set them up by following this explanation of how to set up SSH keys on your local machine.

* Three servers running Ubuntu 20.04 with at least 2GB RAM and 2 vCPUs each. You should be able to SSH into each server as the root user with your SSH key pair.

* Ansible installed on your local machine. If you’re running Ubuntu 20.04 as your OS, follow the “Step 1 - Installing Ansible” section in How to Install and Configure Ansible on Ubuntu 20.04 to install Ansible. For installation instructions on other platforms like macOS or Rocky Linux, follow the official Ansible installation documentation.

* Familiarity with Ansible playbooks. For review, check out Configuration Management 101: Writing Ansible Playbooks.

* Knowledge of how to launch a container from a Docker image. Look at “Step 5 — Running a Docker Container” in How To Install and Use Docker on Ubuntu 20.04 if you need a refresher.

## Step 1 — Creating a Non-Root User on All Remote Servers

`` ansible-playbook -i hosts initial.yml ``

## Step 2 — Installing Kubernetetes’ Dependencies

``ansible-playbook -i hosts kube-dependencies.yml``

## Step 3 — Setting Up the Control Plane Node

``ansible-playbook -i hosts control-plane.yml``

## Step 4 — Setting Up the Worker Nodes

``ansible-playbook -i hosts workers.yml``

