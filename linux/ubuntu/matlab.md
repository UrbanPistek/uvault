# Install Matlab on Ubuntu
Download Installer: https://www.mathworks.com/downloads/
1. Unzip 
2. Open Terminal, run: `xhost +SI:localuser:root`
3. Navigate into the unzipped folder, run `sudo ./install`

During install be sure to create a symbolic link to be able to run matlab using the `matlab` command. 

## Running Matlab
Once installed you can run matlab from the terminal using the following: 
1. `matlab`
2. `/usr/local<PATH TO INSTALL>/bin/matlab -desktop` 
	1. Ex: `/usr/local/MATLAB/R2022a/bin/matlab -desktop`

## Fixing Errors When Running Matlab
There may be a couple errors showing up when you run Matlab that are not impactful, but here is how you can fix them. 

For the following error:
```
Gtk-Message: 08:14:28.995: Failed to load module "canberra-gtk-module"
```

Run: 
```
sudo apt install libcanberra-gtk-module
```

```
sudo ln -s /usr/lib/x86_64-linux-gnu/gtk-2.0/modules/libcanberra-gtk-module.so /usr/lib/libcanberra-gtk-module.so
```

### Add Additional Matlab Support

Create application icon and other support. 
```
sudo apt-get install matlab-support
```


### Resources
* https://www.mathworks.com/matlabcentral/answers/1459909-installer-hang-when-installing-matlab-r2021b-as-root-on-ubuntu-20-04
* https://www.mathworks.com/matlabcentral/answers/472134-gtk-message-10-32-31-466-failed-to-load-module-canberra-gtk-module
* https://askubuntu.com/questions/971560/what-is-the-purpose-of-canberra-gtk-module