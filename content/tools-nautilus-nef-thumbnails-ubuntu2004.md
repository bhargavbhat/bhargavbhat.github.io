Title: NEF Thumbnails in Nautilus
Date: 2020-10-02 20:18
Category: tools
Tags: nautilus, thumbnails, nef
Authors: Bhargav Bhat
Summary: A hacky workaround for getting NEF thumbnails to work in Nautilus on Ubuntu 20.04

Today, I upgraded to the latest Ubuntu LTS 20.04 "Focal" and ran into an annoying bug with Nautilus : `NEF` (Nikon camera raw) files were not having their thumbnails generated, where as this wasn't an issue with 18.04 at all. The issue is a known [bug](https://bugs.launchpad.net/ubuntu/+source/gnome-raw-thumbnailer/+bug/1871862), apparently due to non-availability of a pacakge on 20.04 (based on my very limited understanding).

A bit of searching lead me to this old SO [question](https://askubuntu.com/questions/283072/nautilus-isnt-displaying-thumbnails-for-my-nef-files-photo-raw) that appears to be relevant to the problem I was facing and so down the rabbit hole I go. The first stumbling block was that I couldn't quite find the right file...

```
$ nvim /usr/share/thumbnailers/
atril.thumbnailer  gdk-pixbuf-thumbnailer.thumbnailer  gnome-font-viewer.thumbnailer  librsvg.thumbnailer
```

... the files on my system were quite a bit different from what the top voted answer indicate. However, the files that do showup are similar enough to what's posted in the answer. A little more digging around and `gdk-pixbuf-thumbnailer.thumbnailer` appears to be the best candidate for tweaking and the contents of the file more or less confirm this:

```
$ cat /usr/share/thumbnailers/gdk-pixbuf-thumbnailer.thumbnailer
[Thumbnailer Entry]
TryExec=/usr/bin/gdk-pixbuf-thumbnailer
Exec=/usr/bin/gdk-pixbuf-thumbnailer -s %s %u %o
MimeType=image/png;image/bmp;image/x-bmp;image/x-MS-bmp;image/gif;image/x-icon;image/x-ico;image/x-win-bitmap;image/vnd.microsoft.icon;application/ico;image/ico;image/icon;text/ico;application/x-navi-animation;image/jpeg;image/x-portable-anymap;image/x-portable-bitmap;image/x-portable-graymap;image/x-portable-pixmap;image/tiff;image/x-xpixmap;image/x-xbitmap;image/x-tga;image/x-icns;image/x-quicktime;image/qtif;
```

so... I just append `image/x-nef;image/x-nikon-nef;` to that file, save changes and restart `nautilus` and _viola!_ working thumbnails for `NEF`s. A 10yr old solution still works, more or less :D

PS: Obligatory [xkcd](https://xkcd.com/979/)
