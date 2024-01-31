# Ubuntu Utilities

## Graphics Card

AMD Monitor: 
https://github.com/clbr/radeontop

```
sudo apt install radeontop
sudo radeontop
```

Hit  `c`  to enable colors and  `q`  to quit. 
https://manpages.ubuntu.com/manpages/bionic/man1/radeontop.1.html

Benchmark: 
```
sudo apt install glmark2
glmark2
```

## Ubuntu on a VM
https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview

## Bluetooth Configuration
See file:
```
nvim /etc/bluetooth/main.conf
```

# Download A AppImage

[Source](https://www.itprotoday.com/development-techniques-and-management/why-and-how-use-appimage-ubuntu)

You may have to install FUSE

```
sudo apt-get install fuse libfuse2
```

Download, make it executable & move to a desirable location
```
wget http://somewebsite.com/path/to/YourApp.AppImage
chmod +x YourApp.AppImage
mv YourApp.AppImage /<location>
```

## Create the Desktop Shortcut

Create a `YourApp.desktop` file with the following:
```
[Desktop Entry]
Name=YourApp
Exec=/path/to/YourApp.AppImage
Icon=/path/to/icon.svg
comment=app
Type=Application
Terminal=false
Encoding=UTF-8
Categories=Utility;
```

Make executetable & move to a different location, add icon to your applications
```
sudo cp /home/yourusername/YourApp.desktop /usr/share/applications/
```

# Proton VPN

[Source](https://protonvpn.com/support/official-ubuntu-vpn-setup/)
