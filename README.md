# FiveM Startup Scripts (1.1.0)
Startup scripts for the FiveM server software - uses the "screen" command to manage session. This also restarts the FiveM server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/FiveMStartup)

---

These start up the FiveM server at boot time with a "screen" process.

1. Copy **fivem** into **/home/fivemowner/bin** - make sure it is executable
2. Copy **startfivem** into **/home/fivemowner/fivem** - make sure it is executable
3. Add "**@reboot /home/fivemowner/bin/fvem start**" to the crontab

When you want to view the FiveM console, just enter "**screen -r**" in your shell.

To disconnect from the FiveM console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /home/fivemowner/server-data/nostart**". To reenable it type "**rm /home/fivemowner/server-data/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
