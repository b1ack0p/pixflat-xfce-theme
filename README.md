# PiXflat-xfce-theme

This is Raspberry Pi OS PiXflat modified theme and icons for XFCE. I love the simplicity and clean look of RaspiOS theme so I wanted to modify it for XFCE. it is my self amateur work so I can't say it is perfect but at least it looks like RaspiOS theme very close enough. Any contribution to make it perfect is very welcome.

I mostly kept original PiXflat icons, renamed some of them to adapt to XFCE and added additional icons. I also draw and added some other icons in scalable format. there was no built in battery icons in PiXflat so i draw myself in inkscape but there are some rendering issues in XFCE.  Anyone who can make better battery icons or make my icons better or fix rendering issue is welcome.

For xfwm4 theme I modified Mowi-24 xfwm4 theme and enlarged window title bars to 32px from 24px and made window close/minimize/maximize buttons same with original PiXflat theme. unfortunately after I changed title bar size Mowi xfwm4 theme no longer brought the main PiXflat theme colors so I had to color bars myself. so this also needs fixing. originally Mowi-24 theme takes the colors from main theme. Mowi-24 xfwm4 theme can be downloaded here: https://www.xfce-look.org/p/1700122/

#What is inside:
- font : Default RaspberryPiOS font - Piboto

- gtk-3.0 : contains sample gtk.css file

- icons: 
	.PiXflat: modified PiXflat icons inherits to Gnome icons (you need to install Gnome icons separately)
	.PiX: retro look of PiXflat icons (early RpiOS icons)
	.gnome-icons: contains Gnome icon theme v3.12.0-3 package

- Wallpaper: RaspberryPiOS default wallpapers (rpd-wallpaper)

- theme:
	.PiX theme
	.PiXflat theme (modified gray theme)
	.PiXflat-blue theme (modified blue theme)

#Getting ready:
- Copy icon folders to /usr/share/icons ( example: "sudo cp -r ../icons/PiXflat /usr/share/icons/" )
- Copy "PiX/PiXflat/PiXflat-blue" themes from "themes" folder to /usr/share/themes or ~/.themes in your user dir.
- install "font/fonts-piboto_1.2_all.deb" file which contains official RaspiOS fonts "Piboto"


#Setting theme and icons in XFCE:
- Settings Manager > Appearance > Style > choose one of PiXflat theme
- Settings Manager > Appearance > Icons > PiXflat icons
- Settings Manager > Appearance > Font > Default font > PibotoLt Regular 10
- Settings Manager > Window Manager > choose one of PiXflat for xfwm4 window theme and change Font to PibotoLT Regular
- Settings Manager > Window Manager Tweaks > Compositor > disable "Show shadows under dock windows/regular windows/popup windows/
- Settings Manager > Mouse and Touchpad > Theme > choose PiXflat (I combined default PiXflat cursor icons with https://store.kde.org/p/1416041/)

*NOTE: "PiX" theme is buggy - needs fixing.

*NOTE2: PiXflat icon theme inherits from Gnome 3.12.0-3 icons. You can find Gnome icon theme in the repository directory or you can download from the link below.

*IMPORTANT: to use regular icons instead of symbolic icons as status icons on XFCE panel (this is necessary to get correct colored icons for the status icons such as battery/volume/notification icons otherwise they will appear black and broken) edit or create "gtk.css" in your /home/user/.config/gtk3/gtk.css and add this line ".xfce4-panel image { -gtk-icon-style: regular; }" or copy .css file from /icons/gtk3 to /home/user/.config/gtk3/ folder

you may want to run "sudo gtk-update-icon-cache /usr/share/icons/PiXflat" after selecting icon theme. if you make any change on icon theme run the same command to refresh system.

you may need this also  "sudo apt install gtk2-engines"


#LightDM user image on logon screen:
- uncomment "Hide user greeter image = false" in /etc/lightdm/lightdm.conf
- install "sudo apt install lightdm-gtk-greeter-settings"
- in LightDM GTK Greeter Settings app choose desired user-greeter image (image should be in directory where system can reach, not in /home/user directory)


#Same background on LightDM greeter screen with desktop wallpaper:
- install "sudo apt install accountsservice"
- copy wallpapers you wish to use to /usr/share/backgrounds/anyfolder
- select "Use user wallpaper if available" in LightDM GTK Greeter Settings app


#Original files:
- Non-modified PiXflat theme can be found in : https://github.com/RPi-Distro/raspberrypi-ui-mods
- Non-modified PiXflat icons : http://archive.raspberrypi.org/debian/pool/main/p/pixflat-icons/
- Piboto font : https://archive.raspberrypi.org/debian/pool/main/f/fonts-piboto/
- Gnome icon theme (3.12.0-3): https://packages.debian.org/bullseye/all/gnome-icon-theme/download


#Screenshots:

![Screenshot_2022-06-14_21-10-28](https://user-images.githubusercontent.com/72235930/173660128-cfc71f1c-6cb4-4c55-b235-db4763d5be53.png)

![Screenshot_2022-06-14_21-09-01](https://user-images.githubusercontent.com/72235930/173660075-06240c2c-687f-4cd3-98b8-229b58c9fd04.png)

![Screenshot_2022-06-13_03-08-13](https://user-images.githubusercontent.com/72235930/173259366-db8a723d-2116-410b-81d9-bda779a4ebdf.png)

![Screenshot_2022-05-18_18-14-22](https://user-images.githubusercontent.com/72235930/169077238-0604d2fe-3097-4fbd-ac01-e3fc0fd92570.png)

![Screenshot_2022-05-19_15-57-56](https://user-images.githubusercontent.com/72235930/169299911-8a9e71c2-37a1-489e-a235-e8031f96f192.png)

![Screenshot_2022-05-18_00-22-49](https://user-images.githubusercontent.com/72235930/169033279-ae21e79e-945f-4d19-abe5-b8d9d3ff35a7.png)

![Screenshot_2022-05-18_14-53-34](https://user-images.githubusercontent.com/72235930/169033557-54bbcb68-b254-402d-b5fd-f4038fc3a121.png)
