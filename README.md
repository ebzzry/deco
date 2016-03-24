wp
==

This tiny [Scsh](https://scsh.net) script sets the wallpaper—the root
window image. It features random selection, and timeouts.

To specify an image as a wallpaper:

```
$ wp foobar.jpg
```

To select a random image, from `~/Pictures`:

```
$ wp --random
```

To select a random image, from `/pub/pics/wallpapers`:

```
$ wp --random --directory /pub/pics/wallpapers
```

To select a random image, from `~/Pictures`, with a 5-minute (300
seconds), refresh interval:

```
$ wp --random --timeout 300
```
