# PiXflat-xfce-theme

RaspberryPiOS PiX & PiXflat modified icons and theme for Xfce


LightDM user image on logon window:
- uncomment "Hide user greeter image = false" in /etc/lightdm/lightdm.conf

Same background on LightDM greeter screen with desktop wallpaper:
- install "sudo apt install accountsservice"
- install "sudo apt install lightdm-gtk-greeter-settings"
- copy wallpapers you wish to use to /usr/share/backgrounds/<anyfolder>
- select "Use user wallpaper if available" in LightDM GTK Greeter Settings app
