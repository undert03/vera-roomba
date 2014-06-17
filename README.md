Vera Roomba Plugin Version 1.4.2
===========
![Roomba RooWifi Vera Plugin](https://dl.dropboxusercontent.com/u/617004/Roomba/APPICON_LG.png "Roomba RooWifi Vera Plugin")

Plugin Programmed by undertoe@chemlab.org
Concept based on nitehawk


Plugin Features
-----------

- Clean/Pause and Dock button
- Roomba battery status
- improved Roomba availability (ping)
- Username & Password Support
- Realtime Device Status with UI label
- Multiple Icons for all different levels of status
- True Dock support


Requirements
-----------

Roomba with a Roowifi module (http://www.roowifi.com/).
Roowifi configured to connect with your wireless network, not ad-hoc.

Installation - Vera App Market Place
-----------

- Install from Market Place then follow the configuration instructions

http://apps.mios.com/plugin.php?id=6756

Installation - Manual from GitHub
-----------

- Extract your the Vera Roomba zip file you downloaded from 

- Uploads contents of icons folder to: /www/cmh/skins/default/icons (using WinSCP)

- Uploads contents of libs folder to: /usr/lib/lua (using WinSCP)

- Navigate to apps --> develop apps --> Luup files in vera UI
Add all 4 files under the luup files folder you extracted from the zip
check restart luup after upload

- Reload Vera

- Create a new device (apps --> develop apps --> Create device), in the field "Upnp Device Filename" you enter D_Roomba1.xml, leave the rest empty and click Create Device

- Save and Reload Vera

Configuration
-----------

In the Advanced tab of the plugin

Address : IP Address of your Roowifi
Username: your Roowifi username (default: admin)
Password: your Roowifi password (default: roombawifi)

If you have no password make both the Username and Password field blank

Save and Reload Vera (sometimes multiple reloads necessary)	typically twice for status messages to clean and sync

Screenshots
-----------

![Roomba RooWifi Vera Plugin - Different States](https://dl.dropboxusercontent.com/u/617004/Roomba/Screenshot-2.jpg "Roomba RooWifi Vera Plugin - Different States")

![Roomba RooWifi Vera Plugin - Advance Tab](https://dl.dropboxusercontent.com/u/617004/Roomba/Screenshot-1.jpg "Roomba RooWifi Vera Plugin - Advance Tab")