**Sojourner** is a conference schedule viewer for the [Nokia N900](http://maemo.nokia.com/n900/), the smartphone of choice for the discerning sandal-wearer. Talks can be viewed by topic, by room or by time; your favourite events can be starred for easy browsing later on.

It originally showed the schedule for [FOSDEM](http://fosdem.org/); it has subsequently been made to show others, thanks mainly to wonderful contributors! It's written in *Python* and uses the [Hildon](http://pymaemo.garage.maemo.org/python_hildon_manual/) widget set. Thanks to a really shonky abstraction layer—named *Malvern*—the application also runs with plain [Gtk+](http://www.gtk.org/), though it's not beautiful.

Packaging
---------
To build sojourner debian package you need N900 SDK. The easiest (but probably not the fastest) way to obtain it is to use vagrant. Configuration file can be downloaded from here: https://github.com/silvio/vagrant-n900-sdk

After booting the virtual machine run scratchbox

	scratchbox

Install the package dependencies
	
	fakeroot apt-get install cdbs python2.5 python-central

Build the package (share files between host system and scratchbox via /tmp directory)
	
	dpkg-buildpackage -rfakeroot
