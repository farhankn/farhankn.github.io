---
layout: post
title:  "Burp Extenders Demystified"
description: Introduction to my blog
date:   2020-05-01 13:03:36 +0530
categories: burpsuite
---




### How to add TryHackMe IP address to your menu bar on Kali





`sudo apt install xfce4-genmon-plugin`

add the Generic Monitor panel to your bar with Right Click > Add New Items

Create a shell script with:

```
ADDR=$(ip addr | grep tun0|grep inet|awk '{print $2}'|cut -d "/" -f 1)

echo "$ADDR" | sed 's/$/ /g'
```


set the command field in Generic Monitor to be /location/of/script.sh - I was too lazy to try to get it work all on one line in the genmon command field

in 'Label' field put a single space (for pretty spacing) and change font to whatever

you now have  IP in your panel



