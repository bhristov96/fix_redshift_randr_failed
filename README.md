# How to fix Redshift not working on Debian
This is how to fix Redshift in Debian by disabling Wayland. 

This is done with the editor nano, you can accomplish this with any editor.


In terminal type:

nano /etc/gdm3/daemon.conf

Once the file opens find the line that says '# WaylandEnable=false'. Remove the #, save the file and reboot. 
A fast way to reboot is to type 'poweroff --r' in the terminal

I am working on a way to have a single command to do that in order to simplify the process. My current idea is to do the following:

sed -i -e 's/# WaylandEnable=false/WaylandEnable=false/g' /etc/gdm3/daemon.conf

sed -i -e 's/#WaylandEnable=false/WaylandEnable=false/g' /etc/gdm3/daemon.conf

These two lines of code should handle all possibilities of WaylandEnable being commented out
