# Infrastructure

This project contains Ansible playbooks for configuration of On-board Computer operating system.

The OBC will be equipped with a Raspberry Pi Compute Module 4 and will run on Ubuntu 24.10.


## Setup

1. Install [Poetry](https://python-poetry.org/docs/#installing-with-the-official-installer)

2. Install dependencies:
   ```bash
   poetry install --no-root
   ```

3. Activate the virtual environment:
   ```bash
   $(poetry env activate)
   ```