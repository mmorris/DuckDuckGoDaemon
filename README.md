
What is This?
-------------
This Launch Daemon adds DuckDuckGo support to Safari by editing the /etc/hosts file on Lion. 


How To Install
--------------
1. Copy the com.mattmorris.duckduckgo.plist into /Library/LaunchDaemons/.
2. Reboot [OR] Type the following command in terminal:

`sudo launchctl load /Library/LaunchDaemons/com.mattmorris.duckduckgo.plist`

**Note:** Don't forget to go to Safari Preferences and select Yahoo! as the Default Search Engine.

How to Uninstall
----------------
1. Remove the file: /Library/LaunchDaemons/com.mattmorris.duckduckgo.plist
2. Reboot [OR] Type the following command in terminal:

`sudo launchctl remove com.mattmorris.duckduckgo`


Why isn't it sufficient to just manually edit /etc/hosts file?
--------------------------------------------------------------
It's usually good enough.

But some 3rd party applications tweak /etc/hosts to suit their needs, often removing custom entries. This daemon will continue to watch the /etc/hosts file and will add the entry back instantly if the file is reset by a 3rd party application.

The Cisco VPN client is the most notable example. Yes, you can just add the custom entry to /etc/hosts.ac, but if the software is uninstalled/reinstalled it will get overwritten again.
