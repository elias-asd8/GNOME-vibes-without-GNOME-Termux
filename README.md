# GNOME-vibes-without-GNOME-Termux
Here's a guide to get gnome on xfce (sorta were just installing xfce and installing the gnome components)
so first we need to update pkgs and proot-distro ubuntu, we can do this by executing
```bash
pkg upgrade && pkg install proot-distro && pd install ubuntu && pd login ubuntu && apt upgrade -y
```
now we need our stuff for xfce and the gnome transformation 
```bash
apt install xfce4 xfce4-terminal xfwm4 xfce4-panel thunar xfdesktop4 xfce4-settings xfce4-session xfce4-whiskermenu-plugin plank nitrogen adwaita-icon-theme adwaita-cursors -y
```
ok now we need to get the xserver running (u need the Termux:X11 app from GitHub or f-droid)
```bash
termux-x11 :0 &
```
ok now we start xfce4 
```bash
startxfce4 &
```
Now go to the xpanel (xfce panel) and right click it, click panel, click add new items, search whiskermenu and click on it, then click on the button add
If u want a custom wallpaper u can run in the xfce terminal 
```bash
nitrogen /storage/emulated/0/Pictures/
```
or if its in proot:
```bash
nitrogen ~/
```
ok now run the app bar 
```bash
plank &
```
after running that minimize the terminal
now the icons, we have to go to Settings → Appearance → Icons tab → select Adwaita

then boom! ur xfdesktop is gnome without systemd stuff
anyways yapped too much so cya! :)
