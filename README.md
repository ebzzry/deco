deco
====

This is a trivial [Scsh](https://scsh.net) script that sets the the root window image, commonly
known as the wallpaper. It features random selection and timeouts.


Usage
-----

To specify an image as a wallpaper:

    deco foobar.jpg

To select a random image from `/pub/pics/wallpapers`:

    deco --random --directory /pub/pics/wallpapers

To select a random image from `/pub/bil/deco/chromecast` every 24 hours:

    deco --random --timeout 86400 --directory /pub/bil/deco/chromecast &

To display help and options:

    deco --help