# rebroadcast1090

This repo contains scripts for a Raspberry Pi to bridge data between
existing dump1090-fa and dump978-fa instances to a net-only instance of dump1090-fa.

Each directory is named with the path where the files inside it should reside.

The build script in the main directory will create a new version of dump1090-fa that runs as dump1090-fa2.  This script was originally created by abcd567 and
can be found here:
https://github.com/abcd567a/two-receivers/blob/master/2-receivers-dump-fa.sh

Copy the files and set appropriate ownership and modes and then start the new
services.

Files in /lib/systemd/system should be set to mode 644
Files in /usr/share/dump1090-fa should be set to mode 755 
Files in /etc/default should be set to mode 644

sudo systemctl enable bridge978
sudo systemctl enable bridge1090
sudo systemctl restart bridge978
sudo systemctl restart bridge1090


