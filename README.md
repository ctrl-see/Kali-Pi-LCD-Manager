 ~ ~ ~ ~ ~ ~ ~ Kali Pi LCD Manager ~ ~ ~ ~ ~ ~ ~

Automates install and setup process for LCD-show-kali, as well as forces rotate on restart.

# What this actually does:

1. Updates system + clones necessary LCD drivers.

2. If rotation is requested, a flag file is created.

3. This flag file works in conjunction with bootrotate, which is set up with Cron to execute rotate.sh on detection.

4. Once rotate.sh has been executed, the flag file is deleted.

# Big benefit!

 - If switching to and from HDMI is ever desired, this makes the process much easier.

 - Navigate to:
    ~/Documents/Kali-Pi-LCD-Manager/LCD-show-kali

 - Run:
    sudo ./LCD-hdmi

 - When it is time to leave the big screen, simply navigate back to:
    ~/Documents/Kali-Pi-LCD-Manager/

 - And run:
    ./install

 - That's it!

= = = = = Installation = = = = =

 - Run in terminal:
    cd ~/Documents
    git clone https://github.com/ctrl-see/Kali-Pi-LCD-Manager.git
    cd ./Kali-Pi-LCD-Manager
    chmod +x ./install ./bootrotate
    sudo ./install
