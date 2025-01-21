# Playbook

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