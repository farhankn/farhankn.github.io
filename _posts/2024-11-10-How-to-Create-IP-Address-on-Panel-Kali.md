
How to add TryHackMe IP address to your menu bar on Kali
Resource
sudo apt install xfce4-genmon-plugin

add the Generic Monitor panel to your bar with Right Click > Add New Items

Create a shell script with:

ADDR=$(ip addr | grep tun0|grep inet|awk '{print $2}'|cut -d "/" -f 1)

echo "$ADDR" | sed 's/$/ /g'

