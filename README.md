wp
==

This tiny [Scsh](https://scsh.net) script sets the wallpaper—the root
window image. It features random selection, and timeouts.

## Usage

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


## Important

Please change the shebang line at the top of this program, to reflect
your system. It may be one, or more, of the following:

* `/usr/bin/scsh`
* `/usr/local/bin/scsh`
* `/bin/scsh`
* `/home/user/.nix-profile/bin/scsh`

If you're using [NixOS](https://nixos.org), you may have the following
in your `/etc/nixos/configuration.nix`:

```
environment = {
  systemPackages = with pkgs; [scsh];
};
```

Why not just use `/usr/bin/env scsh`? We can't do that because `env`
does not allow passing arguments to the interpreter, which we need, in
our case.
