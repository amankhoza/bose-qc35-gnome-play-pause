# Support for play pause button on headphones when playing videos in a browser (eg. Netflix, YouTube)

## What the script does

Whilst the script is running it will listen for dbus events, when it detects the play pause button is pressed on the headphones it will simulate pressing the spacebar key (which triggers play pause in most browsers when playing a video).

## Try it out

To get started just clone the repo and run the script:

`git clone https://github.com/amankhoza/gnome-headphone-play-pause-support-in-browser.git`

`cd gnome-headphone-play-pause-support-in-browser`

`./playpause`

Then navigate to Netflix, YouTube etc. and try it out.

In it's current form the script is tailored for Bose QC35 headphones (it may work out of the box with other headphones too, if not read below).

## How to tailor it for other headphones

This is tailored for the dbus signal that gets emitted when I press the play pause on my Bose QC35 headphones. You can modify it to suit your own headphones by running:

`dbus-monitor "path=/org/gnome/Shell,interface=org.gnome.Shell,member=AcceleratorActivated"`

Then press the button on your headphones and look out for something to grep for that uniquely identifies the signal, in my case its "uint32 182", once you find something then modify the grep argument in the `playpause` script accordingly.
