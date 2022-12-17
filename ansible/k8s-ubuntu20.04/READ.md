# ansible playbook for automated installation kubernetes on ubuntu 20.04 server with two workers and a master node

## Install ansible on master node


```shell
apt install ansible
```

## Setting up Ansible to Deploy Kubernetes 1. Change adresses on hosts 2. Run ping pong

```shell
ansible all -m ping
```

## Install Kubernetes on all nodes with dependencies 

```shell
ansible-playbook install-k8s.yml
```

## Creating a Kubernetes Cluster Master Node

```shell
ansible-playbook  master.yml
```

##Join Worker Nodes to Kubernetes Cluster

```shell
ansible-playbook join-workers.yml
```
