# PiXflat-xfce-theme

This is Raspberry Pi OS PiX & PiXflat modified icons and theme for XFCE by myself. it is my self amateur work so I can't say it is perfect but at least it looks like RaspiOS theme very close enough. Any contribution to make it perfect is very welcome.

I used RaspiOS' PiXflat theme / XFCE's default Adwaita theme and Gnome icon themes to create icon theme. there was no built in battery icons in PiXflat so i draw them myself in inkscape but there are some rendering issues in XFCE. Anyone who can make better battery icons or make my icons better or fix rendering issue is welcome.

For xfwm4 theme I modified Mowi-24 xfwm4 theme and enlarged window title bars to 32px from 24px and made window close/minimize/maximize buttons same with original PiXflat theme. unfortunately after I changed title bar size Mowi xfwm4 theme no longer brought the main PiX/PiXflat theme colors so I had to color bars myself. so this also needs fixing. originally Mowi-24 theme takes the colors from main theme. Mowi-24 xfwm4 theme can be downloaded here: https://www.xfce-look.org/p/1700122/


#Getting ready:
- Copy "icons/PiXflat" to /usr/share/icons
- Copy "theme/Pix" and "theme/PiXflat" to /usr/share/themes
- install "fonts-piboto_1.2_all.deb" file in "font" folder


#in XFCE choose theme and icons:
- Settings manager > Appearance > Style > Pix or PiXflat
- Settings manager > Appearance > Icons > PiXflat icons
- Settings manager > Appearance > Font > Default font > PibotoLt Regular 10
- Settings manager > Window Manager > choose Pix or PiXflat for xfwm4 window theme and change Font to PibotoLT Regular
- Settings manager > Window Manager Tweaks > Compositor > disable "Show shadows under dock windows/regular windows/popup windows/
- to use regular icons instead of symbolic icons as status icons on XFCE panel (this is necessary to get correct colored icons for the status icons such as battery/volume/notification icons otherwise they will appear black and broken) edit or create "gtk.css" in your /home/user/.config/gtk3/gtk.css and add this line ".xfce4-panel image { -gtk-icon-style: regular; }" or copy .css file from /icons/gtk3 to /home/user/.config/gtk3/ folder

you may want to run "sudo gtk-update-icon-cache /usr/share/icons/PiXflat" after selecting icon theme. if you make any change on icon theme run the same command to refresh system.

you may need this also  "sudo apt install gtk2-engines"

#LightDM user image on logon window:
- uncomment "Hide user greeter image = false" in /etc/lightdm/lightdm.conf
- install "sudo apt install lightdm-gtk-greeter-settings"
- in LightDM GTK Greeter Settings app choose desired user-greeter image (image should be in directory where system can reach, not in /home/user directory)


#Same background on LightDM greeter screen with desktop wallpaper:
- install "sudo apt install accountsservice"
- copy wallpapers you wish to use to /usr/share/backgrounds/anyfolder
- select "Use user wallpaper if available" in LightDM GTK Greeter Settings app
