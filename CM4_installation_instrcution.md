## Hardware requirement
1. Jumper for goldpin
2. Micro-usb cable
3. Compute Module 4
4. Compute Module 4 IO Board
5. 12V power suply caple
   
## Step 1
1. Connect two golpins in the top left Board (described as "Fit jumper to disable eMMC Boot)
2. Power up compute module
3. Connect to your computer

## Step 2
1. Download the repository: https://github.com/raspberrypi/usbboot
2. On bubntu computer write command:
```bash
sudo apt install -y libusb-1.0-0-dev
```
3. Go to folder in which you have your downloaded repository and put
```bash
make
```
This will create  **rpiboot**
4. Write command:
```bash
sudo ./rpiboot 
```   
which will boot eMMC into usb mass stage mode and you will see drive pop up on your screen
## Step 3
1. Use Rapberry Pi Imager to flash you Compute Module. In instruction **RB_installation_instruction.md** is tutarial how to do it

## Step 4 - addition
If you want to use the antena add to **/boot/firmware/config.txt**:
```bash
dtparam=ant2