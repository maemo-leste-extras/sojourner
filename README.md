**Sojourner** is a conference schedule viewer for the [Nokia N900](http://maemo.nokia.com/n900/), the smartphone of choice for the discerning sandal-wearer. Talks can be viewed by topic, by room or by time; your favourite events can be starred for easy browsing later on.

It originally showed the schedule for [FOSDEM](http://fosdem.org/); it has subsequently been made to show others, thanks mainly to wonderful contributors! It's written in *Python* and uses the [Hildon](http://pymaemo.garage.maemo.org/python_hildon_manual/) widget set. 

This software was created by [Will Thompson](http://willthompson.co.uk/) and he deserves all the credit; I just fix critical bugs and make new releases.

Download
--------
This app can be downloaded directly from extras-devel or extras-testing [Maemo repository](http://maemo.org/packages/view/sojourner/). Alternatively binary debian package can be downloaded from [Releases page](https://github.com/loomchild/sojourner/releases).

Packaging
---------
To build sojourner debian package you need N900 SDK. The easiest (but probably not the fastest) way to obtain it is to use vagrant. Configuration file can be downloaded from here: https://github.com/silvio/vagrant-n900-sdk

After booting the virtual machine run scratchbox

	scratchbox

Install the package dependencies
	
	fakeroot apt-get install cdbs python2.5 python-central

Build the package (share files between host system and scratchbox via /tmp directory)
	
	dpkg-buildpackage -rfakeroot

More info about these commands can be found here: http://wiki.maemo.org/Documentation/Maemo_5_Developer_Guide/Packaging,_Deploying_and_Distributing

Uploading
---------
The package upload process is described here: http://wiki.maemo.org/Uploading_to_Extras-devel

I use extras assistant: https://garage.maemo.org/extras-assistant/index.php

Issues
------
To report bugs or request a feature please go to my [Trac](http://trac.loomchild.net/sojourner), register a new user account and post the issue.

