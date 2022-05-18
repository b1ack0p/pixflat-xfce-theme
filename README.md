# PiXflat-xfce-theme

RaspberryPiOS PiX & PiXflat modified icons and theme for XFCE

- Copy "icons/PiXflat" to /usr/share/icons
- Copy "theme/Pix" and "theme/PiXflat" to /usr/share/themes
- install "fonts-piboto_1.2_all.deb" file in "font" folder


#in XFCE choose theme and icons:

- Settings manager > Appearance > Style > Pix or PiXflat
- Settings manager > Appearance > Icons > PiXflat icons
- Settings manager > Appearance > Font > Default font > PibotoLt Regular 10
- Settings manager > Window Manager > choose Pix or PiXflat for xfwm4 window theme
- Settings manager > Window Manager Tweaks > Compositor > disable "Show shadows under dock windows/regualar windows/popup windows/
- edit or create "gtk.css" in your /home/user/.config/gtk3/gtk.css and add this line: .xfce4-panel image { -gtk-icon-style: regular; }
- or copy css file from /icons/gtk3 folder here.


#LightDM user image on logon window:

- uncomment "Hide user greeter image = false" in /etc/lightdm/lightdm.conf
- install "sudo apt install lightdm-gtk-greeter-settings"
- in LightDM GTK Greeter Settings app choose desired user-greeter image (image should be in directory where system can reach, not in /home/user directory)


#Same background on LightDM greeter screen with desktop wallpaper:

- install "sudo apt install accountsservice"
- copy wallpapers you wish to use to /usr/share/backgrounds/anyfolder
- select "Use user wallpaper if available" in LightDM GTK Greeter Settings app
