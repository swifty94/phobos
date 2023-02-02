
The Phobos telegram bot is completely a Bash-written one. Hence Linux systems only are supported.
--------------------------------------------------------------------------------------------------

Once it is installed you will be able to receive the notification regarding the server performance at the chosen time frame.
Regular updates will be regarding the following points:
- currently logged users
- number of established connections to the server and to the database
- RAM usage
- Occupied disc space
- CPU usage and top 10 processes which are consuming the CPU

Alert updates in case:
- Apache / MySQL / VSFTPD services are down
- The CPU usage is more than 75% on the server

Pre-requirements
-----------------
- Register your Telegram bot here https://telegram.me/botfather
More details can be checked here - https://core.telegram.org/bots#6-botfather

- Obtain your token as described in the link above + your API URL to getUpdates method which looks like:
https://api.telegram.org/bot{YOURTOKEN}/getUpdates

- Start your bot


Installation:
--------------

wget https://raw.githubusercontent.com/swifty94/phobos/master/phobos_install -O phobos_install && bash phobos_install

Installation process:
------------------------
![](https://raw.githubusercontent.com/swifty94/phobos/master/usg/phobos_install.gif)

!Attention!
Kindly update the respective variables TOKEN and APIURL in the phobos and phobos_stanalone files in order to receive the notifications

Examples of usage and output:
------------------------

- in case the services are down and the CPU load is critical 

![](https://raw.githubusercontent.com/swifty94/phobos/master/usg/alert.png)

- a regular update from bot 

![](https://raw.githubusercontent.com/swifty94/phobos/master/usg/upd.png)

The content of the top file is just the regular top command output.

Content of process file example:

master 7.3 /usr/lib/firefox/firefox\
master 5.3 /usr/lib/firefox/firefox\
master 5.1 /usr/bin/gnome-shell\
master 3.6 Telegram\
master 3.1 /usr/lib/xorg/Xorg\
master 3.1 /usr/bin/pulseaudio\
master 2.8 /snap/whatsdesk/17/whatsdesk\
master 2.3 /usr/lib/firefox/firefox\
master 2.3 /usr/lib/firefox/firefox\
master 2.3 /proc/self/exe
