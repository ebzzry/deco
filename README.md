deco
====

This simple [Scsh](https://scsh.net) script sets the the root window image. It features
random selection and timeouts.


Usage
-----

To specify an image as a wallpaper:

    $ deco foobar.jpg

To select a random image, from `~/Pictures`:

    $ deco --random

To select a random image, from `/pub/pics/wallpapers`:

    $ deco --random --directory /pub/pics/wallpapers

To select a random image, from `~/Pictures`, with a 5-minute (300 seconds), refresh interval:

    $ deco --random --timeout 300
