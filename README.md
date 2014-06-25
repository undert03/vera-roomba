Vera Roomba Plugin Version 1.4.4
===========
![Roomba RooWifi Vera Plugin](https://dl.dropboxusercontent.com/u/617004/Roomba/APPICON_LG.png "Roomba RooWifi Vera Plugin")

Plugin Programmed by undertoe@chemlab.org

Plugin Features
-----------

- Clean/Pause and Dock button
- Roomba battery status
- Improved Roomba availability (ping)
- Username & Password Support
- Realtime Device Status with UI label
- Device Status Triggers
- Schedule Cleaning Mode for Trigger Alerts
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

- Extract your the Vera Roowifi Roomba zip file you downloaded from here 

- Uploads contents of icons folder to: /www/cmh/skins/default/icons (using WinSCP)

- Uploads contents of libs folder to: /usr/lib/lua (using WinSCP)

- Navigate to apps --> develop apps --> Luup files in vera UI

- Add all 4 files under the luup files folder you extracted from the zip *check restart luup after upload

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

Configuration for Scheduled Cleaning
-----------

- Create your Scene where you set the desired Roomba to Clean
- Click the LUUP tab
- Paste the following 

```
luup.variable_set("urn:undertoe-us:serviceId:Roomba1", "ScheduledClean", 1, YOUR_ROOMBA_DEVICE_ID )
```

* YOUR_ROOMBA_DEVICE_ID can be found by clicking on the Settings (Wrench Icon) of your device, then the advance tab. Where it says "Device #111" 111 would be your device id.

There are trigger options now for schedule cleaning ( Started, Completed, Interrupted, Failed) that are now active when you
start your scenes with the above method. So you can now be alerted if your Roomba actually completed after you scheduled a clean.

Also useful for shutting down your HVAC fan during cleaning if you want to prevent dust from getting kicked up and circulated through your
house.


Screenshots
-----------

![Roomba RooWifi Vera Plugin - Different States](https://dl.dropboxusercontent.com/u/617004/Roomba/Screenshot-2.jpg "Roomba RooWifi Vera Plugin - Different States")

![Roomba RooWifi Vera Plugin - Advance Tab](https://dl.dropboxusercontent.com/u/617004/Roomba/Screenshot-1.jpg "Roomba RooWifi Vera Plugin - Advance Tab")

![Roomba RooWifi Vera Plugin - Scene Triggers](https://dl.dropboxusercontent.com/u/617004/Roomba/Roomba-Triggers.jpg "Roomba RooWifi Vera Plugin - Scene Triggers")

Credit
-----------

concept based on nitehawk original work.