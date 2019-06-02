Installation on Pi Zero W (headless usb ssh without need for any addtional wifi adapter/monitor/keyboard)
1. Download Raspbian Stretch Lite
2. Use ethcer to write image to SD card
3. Mount SD card on computer and add an extensionless file "ssh" to the boot folder
3. Follow this guide to allow ssh over USB (https://desertbot.io/blog/ssh-into-pi-zero-over-usb)
4. Connect to computer (Allow first boot some time) and connect to Rpi using ssh
5. Add wifi for initial file downloading by typing command "sudo raspi-config"
6. After entering wifi details using "Network options", Exit raspi-config
7. Now customary "sudo apt-get update"
8. Install Node on pi
9. Follow instructions on main page of Tuya convert to install pre-requisites
10. Now before starting the flash process (./start_flash.sh), run "sudo killall wpa_supplicant" (this will kill wifi connection so that Tuya-Convert can create a wifi)(ssh will not be lost as we're doing that via usb)
11. Let Tuya-Convert do it's job. Enjoy!
