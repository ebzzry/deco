deco
====

This is a simple [Scsh](https://scsh.net) script that sets the the root window image, commonly known
as the wallpaper. It features random selection and timeouts.


Usage
-----

To set `wallpaper.jpg` from the current directory as wallpaper:

    deco wallpaper.jpg

To set a random wallpaper from `~/Pictures/wallpapers/`:

    deco --random --directory ~/Pictures/wallpapers/

To set a random wallpaper from `~/Pictures/wallpapers/` every 24 hours:

    deco --random --timeout 86400 --directory ~/Pictures/wallpapers/ &

To set a random wallpaper from [Wallhaven](https://alpha.wallhaven.cc/):

    curl -so /tmp/wh.jpg -L https://wallhaven.now.sh/random; deco /tmp/wh.jpg; rm -f /tmp/wh.jpg

To display help and options:

    deco --help
