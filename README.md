# OBC System

This project contains Ansible playbooks for configuration of On-board Computer operating system.

The OBC will be equipped with a Raspberry Pi Compute Module 4 and will run on Ubuntu Server 24.4.5 LTS.


## Setup Ansible

1. Install [Poetry](https://python-poetry.org/docs/#installing-with-the-official-installer)

2. Install dependencies:
```bash
poetry install --no-root
```

3. Set correct IP address for your Raspberry Pi in the `inventory.ini`:
```
[raspberry_pi]
raspberry ansible_host=192.168.1.100 ansible_user=ubuntu
```

4. Copy ssh keys to Raspberry Pi if you haven't done so before.
```
ssh-copy-id ubuntu@192.168.1.100
```

5. Activate the virtual environment:
```bash
$(poetry env activate)
```

6. Run the Hello World playbook:
```bash
ansible-playbook playbooks/ping.yml
```
