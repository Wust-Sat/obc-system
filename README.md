# Infrastructure

This project contains Ansible playbooks for configuration of On-board Computer operating system.

The OBC will be equipped with a Raspberry Pi Compute Module 4 and will run on Ubuntu 24.10.


## Setup Ansible

1. Install [Poetry](https://python-poetry.org/docs/#installing-with-the-official-installer)

2. Install dependencies:
```bash
poetry install --no-root
```

3. Activate the virtual environment:
```bash
$(poetry env activate)
```

4. Set correct IP address for your Raspberry Pi in the `inventory.ini`: 
```
[raspberry_pi]
raspberry ansible_host=192.168.1.100 ansible_user=ubuntu
```

5. Run the Hello World playbook:
```bash
ansible-playbook playbook/ping.yml
```
