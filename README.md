vera-roomba
===========

Vera Roomba Plugin Version 1.4.1

All orginal credit goes to 
nitehawk http://forum.micasaverde.com/index.php?action=profile;u=21978
revisions and patcheds made by: undertoe undertoe@chemlab.org


Plugin Features:

Clean and Dock button.
Roomba battery status.
Roomba availability (ping).
Username & Password Support
True Device Status

Requirements:

Roomba with a Roowifi module (http://www.roomba-wifi-remote.com/).
Roowifi configured to connect with your wireless network, not ad-hoc.

Install 1.4 only:

Extract Roombaplugin14.zip 

Uploads contents of libs folder to: /usr/lib/lua (using WinSCP)

Navigate to apps --> develop apps --> Luup files in vera UI
Add all 4 files under the luup files folder you extracted from the zip
check restart luup after upload

Reload Vera

Create a new device (apps --> develop apps --> Create device), in the field "Upnp Device Filename" you enter D_Roomba1.xml, leave the rest empty and click Create Device

Save and Reload Vera

In the Advanced tab of the plugin you enter the 
ip address of the Roowifi in the Address field
if you have a password protected Roomba Wifi you can add your
username and password in the 
Username and Password field under advanced settings
It defaults to the RooWifi default (admin / roombawifi)
If you have no password make it blank

Save and Reload Vera (sometimes multiple reloads necessary)	