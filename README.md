# ubuntu-rpi-configuration
Installing Ubuntu Server, Docker, k3s and other tools for networking on Raspberry Pi 3 B+

Software:

Raspberry Pi Imager (https://www.raspberrypi.com/news/raspberry-pi-imager-imaging-utility/)

Steps:

Download Ubuntu Server Image:

Visit the Ubuntu download page (https://ubuntu.com/download/raspberry-pi) and select the latest Ubuntu Server image for Raspberry Pi 3 (64-bit architecture is recommended).
Flash the Image:

Using Raspberry Pi Imager:
Install the Raspberry Pi Imager on your computer (https://www.raspberrypi.com/news/raspberry-pi-imager-imaging-utility/).
Launch the Imager, select "CHOOSE OS," and browse to "Other general-purpose OS."
Choose "Ubuntu" and select the downloaded image.
Insert your microSD card, select it under "CHOOSE STORAGE," and click "Write."
Important: This will erase all data on the card. Ensure you have backups.


Insert the flashed SD card into your Raspberry Pi 3 B+, connect the HDMI cable to a monitor, plug in the power supply, and connect a keyboard and mouse.
The Raspberry Pi will boot up, and you'll be presented with the Ubuntu Server installation process.

Installation Process:

Follow the on-screen prompts to configure the language, keyboard layout, time zone, user account, and password.
Choose the "Minimal install" option when prompted.
Complete the remaining installation steps and wait for the process to finish.
The Raspberry Pi will automatically reboot upon completion.
Post-Installation Configuration:

Update and Upgrade Packages:

Bash
sudo apt update
sudo apt upgrade 
yes

Set a Static IP Address (Optional):


Install Docker and Docker Engine using my gist:

curl https://gist.githubusercontent.com/gajenderyadavv/6498d66cd446f5818ad9226c155be852/raw/96956a41acafa43c7efe0a117b0f9b685cb80425/install-docker-unix | bash

Installing k3s (Lightweight Kubernetes):

Add the k3s repository:

curl -sSL https://get.k3s.io | sh -s

For other Kubernetes Components and configurations:

curl https://gist.githubusercontent.com/gajenderyadavv/ab485756819e5e2cb0d7d9f4956ec1d7/raw/4d1d262e4cafa243abc72d2218816d67a7e040ac/install-k8s-unix | bash

Also configured git using acces token and served projects of K8s and Docker from my GitHub profile.