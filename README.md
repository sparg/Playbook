# Playbook



## Description: This script performs the following tasks:
### 1. Connects to a remote server using SSH.
### 2. Executes a series of commands on the remote server.
### 3. Retrieves the output of the executed commands.
### 4. Handles any errors that occur during the SSH connection or command execution.
### 5. Closes the SSH connection after the commands have been executed.

### Note:
Variables related to Docker repositories:
The variables may vary depending on the virtual machine (VM) distribution.

## Steps
Steps for proper execution and verification of the code to be executed.

### Test the SSH connection
```bash
ssh usr@10.20.30.40 -i private_key
```

### Run script
```bash
ansible-playbook -i /home/usr/Playbook/inventory.ini /home/usr/Playbook/install_docker.yml
```

### Verify the installation
```bash
sudo docker --version
```

### Docker Response
```bash
usr@linux:~$ sudo docker --version
Docker version 27.5.0, build a187fa5
```