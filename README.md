# PC-to-NAS-Project
Repo for personal project, see readme for more details.

Overview:
-  My intention is to convert an old pc, that would otherwise be recycled, into a NAS and see where I can go from there.
-  The main reason (other than just learning) is that the pc has been sat in its box unused since 2016, so the specs aren't particularly impressive but it seemed a shame to just get rid of it since no one I know needs it and even if they did it wouldn't be able to get windows security updates (windows 7).
-  I'll be using a Linux distribution for the security reason mentioned above and since it is the more efficient of the options I am familiar with it'll work best considering the old specs.
-  This repo will contain my planning and work for this project e.g. screenshots of my process, research, etc.

I have added an images folder for screenshots from the process, at the moment it has the cmd commands I used to setup samba on the pc for file sharing with my main pc which runs on windows.
The mains steps after installing the OS were: 
  -  Creating a folder for the data.
  -  Setting a static IP for the device.
  -  Installing samba.
  -  Setting a samba user profile, for a base level of security even with it only being accessible on my home network at the moment (not looked at VPN potential for remote connection).

I have added a second drive from an even older pc, so now have twice the storage accessible in the nas pc.
Other than formatting the drive after copying documents to another drive, same process as setting up other drive i.e. mount drive, create folder and then add to the samba config.
Note:
  - Will look at wake-on-lan another time, probably tomorrow as of writing this; seems relatively straight forward.
  - Also look at a way to turn it off remotely (I know it can be done via windows cmd but making a program might be more interesting e.g. automatically turns it off if nothing received for a few minutes).
  - I have seen an example of how it can be done via a program (wake-on-lan -> open folder to use -> trigger shutdown remotely) but will need to look at it more another time.

Wake-on-LAN now set up for the pc, I use WakeMeOnLAN[1] (NirSoft) to wake the pc and then currently just using cmd to connect to the pc and shut it down as follows:
  -  ssh user_name@ip
  -  sudo poweroff
I researched this using ArchWiki[2] and SuperOps[3] mainly for the process, not the commands themselves since I did it a different way, I found WakeMeOnLAN via just searching wake on LAN GUI and then doing background research on the options.

References:
[1] N. Sofer. WakeMeOnLAN v1.96. NirSoft. Accessed: 17-09-26 [Online]. Available at: https://www.nirsoft.net/utils/wake_on_lan.html
[2] Manifold (Page Creator). Wake-on-LAN. ArchWiki. Accessed: 13-09-26 -- 16-09-26 [Online]. Available at: https://wiki.archlinux.org/title/Wake-on-LAN
[3] L. Madhu. What is Wake-on-LAN (WoL)? A complete guide to remote power-on. SuperOps. Accessed: 13-09-26 -- 17-09-26 [Online]. Available at: https://superops.com/tech-hub/what-is-wake-on-lan 
