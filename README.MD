# Warning
We're not responsible for bricked devices, missing recovery partitions, dead xiaomi factoryline workers cowboys, dead microSD cards, dead pmics, dead ram, dead display ics, dead cpus, any xiaomi shenanigans, dead cats or dogs, nuclear wars or you getting fired because you forgot to boot back in to android for the alarm.

All the files here have been contributed by other users, here you will find a guide with the working files we managed to get. This is a delicate process, do it under your own risk and follow all the steps carefully.

**IF YOU AREN'T COMFORTABLE MODDING YOUR TABLET OR ITS PARTITION TABLE OR YOU ARE PARANOID OF BRICKING YOUR DEVICE CLICK AWAY NOW!!! YOU HAVE BEEN WARNED, YOU ARE ON YOUR OWN IF YOU BRICK YOUR DEVICE!!! AGAIN! YOU HAVE BEEN WARNED!!!**

# Installation Guide GNOME Shell Mobile for Debian 13 ARM64
Please follow the guide carefully

1. Download gsd-mobile.deb, mutter-mobile.deb and gnome-shell-mobile.deb from releases
2. Install dependencies
    ```bash
    sudo apt-get install gdm3
	sudo apt-get build-dep -y gnome-shell mutter gnome-settings-daemon
	```
3. Install deb files
    ```bash
	sudo apt-get install -y ./*deb --allow-downgrades -o Dpkg::Options::="--force-overwrite"
	```

4. You have to hold those packages, because they are not official from the official Debian repos.
    ```bash
	sudo apt-mark hold gnome-shell mutter gnome-settings-daemon
	```

5. Start service and reboot device
    ```bash
	sudo systemctl enable gdm
    sudo systemctl start gdm
    sudo reboot
	```