# fix_redshift_randr_not_found
This is how to fix Redshift in Debian by disabling Wayland. 

This is done with the editor nano, you can accomplish this with any editor.


In terminal type:

nano /etc/gdm3/daemon.conf

Once the file opens find the line that says '# WaylandEnable=false'. Remove the #, save the file and reboot. 
A fast way to reboot is to type 'poweroff --r' in the terminal

