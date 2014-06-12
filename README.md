Vera Roomba Plugin Version 1.4.2
===========

All orginal credit goes to 
nitehawk http://forum.micasaverde.com/index.php?action=profile;u=21978
revisions and patches made by: undertoe undertoe@chemlab.org


Plugin Features
-----------

- Clean/Pause and Dock button
- Roomba battery status
- improved Roomba availability (ping)
- Username & Password Support
- Realtime Device Status with UI label
- True Dock support


Requirements
-----------

Roomba with a Roowifi module (http://www.roowifi.com/).
Roowifi configured to connect with your wireless network, not ad-hoc.

Installation
-----------

- Extract your the Vera Roomba zip file

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

Save and Reload Vera (sometimes multiple reloads necessary)	