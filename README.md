weed.theme - XChat based theme for irssi
==============

Designed to be the most beautiful irssi theme in the world.
--------------

![weed.theme on OS X Mavericks](https://raw.githubusercontent.com/ronilaukkarinen/weed/master/screenshots/screenshot-mac.png "Screenshot")

**Weed?** Yeah, I have no idea where I got that from (no, I am not smoking). I guess I was watching the grass grow. Around 2006 or 2007 I was frustrated with all the irssi themes I had tried and decided to start designing my own. 

Weed was maybe fifth or sixth theme I did. When nothing pleased me, not even my own previous themes, finally the gem was born. I have not used any other irssi theme ever since. For me and many other users weed.theme is the best irssi theme there is.

Feel free to edit to your needs but I would be pleased if you credited or thanked me in some way! (for example /msg rolle at quakenet)

Thanks for visiting.
If you like it, follow me in twitter to know more about my projects (some of them IRC related): http://twitter.com/rolle

Old changelog
--------------

In case if you want to know what was done before theme ending up in here Github.

- **4.0** *(2013-03-25)* Theme translated in english, added old changelog and tutorial in this Readme. Newer changes and versions will be in commits only.
- **3.6** *(2010-11-27)* Fixes to make theme even more readable. Query layout is now the same than the rest of the windows.
- **3.5** Readability fixes. Spaces made shorter between separator pipes and the timestamps.
- **3.05** Edited pubmsgnick, pubnick, pubmsgmenick, pubmsghinick and = "sb_awaybar";
- **3.00** Added whole new tutorial inside the theme. No changes to the theme itself.
- **2.75e** Tutorial enhanced. 
- **2.75d** Created changelog. Better hilight.

Requirements
--------------

- Linux or unix shell
- irssi (preferably original irssi that comes with your Linux distribution, not tested on irssi for Windows)
- wget (usually with every Linux distribution)
- screen (usually with every Linux distribution)
- git (optional)
- nano/pico (you can also use vi, but the tutorial below is for nano)
- PuttyTray or any command line interface you have in your Linux box, depends are you using shell or your client PC
- Some patience and basic Linux command line knowledge

Installation
--------------

Make backup of your current irssi setup, if you have one, by **cp -Rv ~/.irssi ~/.irssi-backup**. If something goes wrong, you can easily restore it by quitting irssi and running **rm -rf ~/.irssi && mv ~/.irssi-backup ~/.irssi** and running irssi again.

Make sure you are in your home directory by typing **cd ~** and start irssi for the first time (assuming this is clean installation)
`screen irssi`

And then in irssi:
`/save`

You'll see default irssi theme (blue), but get back by pressing **CTRL+A+D**, for now. Clone this repository by using command 
`git clone https://github.com/ronilaukkarinen/weed.git weed-master`

Or if you don't have permissions to install git, run following
`wget --no-check-certificate https://github.com/ronilaukkarinen/weed/archive/master.tar.gz`

And unpack it using

`tar -xvf master.tar.gz`

Copy the theme by running
`cp ~/weed-master/weed.theme ~/.irssi/`

Scripts by running
`mkdir -p ~/.irssi/scripts && cp ~/weed-master/scripts/* ~/.irssi/scripts/`

And finally the modified config by running 

`cp ~/weed-master/config ~/.irssi/`

Then go to irssi by **screen -dr** and run

`/reload` and `/run awl.pl`

You will need to edit your colors to get the final touch (screenshot: http://www.pulina.fi/wp-images/weed-varit.png)

In Putty only **ANSI BLACK** is required to be changed to **25 25 25**.

**Basically you are now done!** You can connect to servers and do whatever you like. However...

Because this is a modified config, your nick and name are **yourname**. Please change your nick by using `/nick something` and `/set user_name something` and your real name by `/set real_name Real Name`. Then type `/save` and `/quit` and start `screen irssi` again.

Optionally you can `/run usercount.pl` and `/sbar awl_0 add -before awl_0 -alignment left usercount` and get a nice usercount on the left.
`/run trackbar.pl` gets you nice bar to separate old and new conversations. If you like it to fit feed more instead of that default grey, run `/set trackbar_string _` and `/set trackbar_style %r`

Really matter of taste, but if you'd like a weed awaybar (big red block in the right), you can add it by `/run awaybar.pl` and `/sbar statusbar add -after erotin -alignment right awaybar` commands. Another truly optional scripts are `/run nicklist.pl` and `/nicklist screen` (enables nicklist) and `/run nickcolor.pl` (every nick in different color).
