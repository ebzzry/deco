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

To set a random Wallhaven wallpaper:

    curl -Ls -O -w %{url_effective} https://wallhaven.now.sh/random | xargs -I % curl -so ~/.deco %; deco ~/.deco

To set a random Chromecast wallpaper:

    curl -s https://raw.githubusercontent.com/dconnolly/chromecast-backgrounds/master/README.md | sed -e 's/^\!\[\](\(.*\))$/\1/' | shuf -n 1 | xargs -I % curl -so ~/.deco %; deco ~/.deco

To display help and options:

    deco --help
