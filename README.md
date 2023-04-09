# dotefiles-bspwm
My bspwm config files
To use my dotefiles you have to install following packages:
1. ```sudo pacman -S bspwm sxhkd polybar pacman-contrib ttf-font-awesome siji-git```
2. Copy all the folder in the .config directory then you are good to to.
![bspwm](bsp.png)

# Tips:
1. Enable touchpad Tap-to-click:
If you are a laptop user, you might want to enable tap to click so that it gets easier to navigate using a touchpad.
It is pretty easy to do so! Copy and paste this one command in your terminal to
fly!<br>
```bash
sudo mkdir -p /etc/X11/xorg.conf.d && sudo tee <<'EOF' /etc/X11/xorg.conf.d/90-touchpad.conf 1> /dev/null
Section "InputClass"
        Identifier "touchpad"
        MatchIsTouchpad "on"
        Driver "libinput"
        Option "Tapping" "on"
EndSection

EOF
```

# To enable touch screen on firefox
```bash
echo export MOZ_USE_XINPUT2=1 | sudo tee /etc/profile.d/use-xinput2.sh
```

# Fonts:
* Iosevka
* noto-fonts
* ttf-font-awesome
* icomoon-feather



# To install Music player mpd & ncmpcpp
step 1. Install mpd and ncmpcpp
step 2. create directory ~/.mpd/mpd.conf. [Link to mpd.conf](https://pastebin.com/raw/mGuS7TZU)
step 3 create some files with ```touch mpd.pid mpd.db mpd.log ```
setp 4. create directory ~/.ncmpcpp/config [link to the ncmpcpp](https://pastebin.com/raw/hiKTfz4i)
step 5. run the command: `` sudo systemctl start mpd``
setp 6. check if it is running with this command: ``systemctl status mpd``
step 7. run this command: `` systemctl --user enable mpd.service``
step 8. type the command: ``mpd`` if no music is showing press the key *2* or *U* to update the database.
then you're good to go.
Video Link for help: [YouTube](https://www.youtube.com/watch?v=F8fnYjYe5bU)





