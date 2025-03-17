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
1. Now after putting SD card into raspberry you can ping your raspberry: **ping (hostname).local**.
2. If ping doesn't work try to redo all steps or wait some more time.
   
## Step 4 - conneting via ssh
**ssh ubuntu@(hostname).local**