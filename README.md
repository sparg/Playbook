# Playbook

## System Architecture Description

This repository contains the configuration and documentation for a web service architecture using HAProxy, WordPress, and MySQL, all hosted on an Azure virtual machine and managed with Docker.

## Architecture Diagram

Below is a diagram describing the system architecture:

```mermaid
graph LR;
  Internet -->|Frontend| A[HAProxy];
  A -->|Backend| B[WordPress];
  B -->|Database| C[(MySQL)];

  subgraph Azure [VM with public IP]
    subgraph Docker [Docker]
      A; B; C;
    end
  end
```

## SSH connection

```bash
ssh usr@10.20.30.40 -i private_key
```

## Run script

### Deploy Docker
```bash
ansible-playbook -i inventory.ini -e @env.yml deploy_docker.yml
```
### Deploy HAProxy - MySQL - WordPress
```bash
ansible-playbook -i inventory.ini -e @env.yml deploy_all.yml
```
