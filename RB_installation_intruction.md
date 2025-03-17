## Step 1 Software installation
Install [*Raspberry Pi Imager*](https://www.raspberrypi.com/software/)
## Step 2 - Open Raspberry PI Imager
1. Choose device: *Raspberry PI 4* or *Raspberry PI 5* depending on your device.
2. Operating System: *UBUNTU SERVER 24.04.5 LTS (64-BIT)* .
3. Storage: *SD CARD*.
Then click **Next**
## Step 3 - EDIT SETTINGS
0. Write down hostname.
1. Set username and password to **ubuntu**.
2. Enable SSH via password.
3. Configure wireless LAN to your local network
 click **SAVE** and **YES** and **YES**.
4. Now after putting SD card into raspberry you can ping your raspberry: 
```bash
ping (hostname).local
```
5. If ping doesn't work try to redo all steps or wait some more time.
   
## Step 4 - conneting via ssh
```bash
ssh ubuntu@(hostname).local
```
## Step 5 - coping ssh key
1. Check if you have public ssh_key: 
```bash
cat ~/.ssh/id_rsa.pub 
```
   if not generate it by running: 
```bash
ssh-keygen -o
```
2. Now you can copy you public key: 
```bash
ssh-copy-id ubuntu@(hostname).local
```
3. Now you don't log in every time you want to connect via ssh to your raspberry.
## Step 6 - playing playbook
1. Change raspberrypi ip adress in **inventory.ini** to match your own raspberry pi ip. You can check it via:
```bash
ifconfig
``` 
2. Activate virtual env:
```bash
$(poetry env activate)
```
3. Now run your playbook:
```bash
ansible-playbook playbooks/ping.yml
```