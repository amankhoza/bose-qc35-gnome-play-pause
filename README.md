# Bose QC35 play pause support for GNOME

Whilst the script is running it will listen for dbus events, when it detects the play pause button is pressed on the headphones it will simulate pressing the spacebar key (play pause in most online and local video player apps).

Main use case is to run the script in the background when you are playing a video online or in an app that doesnt already support play pause via the headphones (eg. Netflix in a browser), if you run the script during video playback on a supported app (eg. VLC) it will not work as play / pause will get triggered twice.
