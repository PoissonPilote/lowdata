# lowdata

This repository is design to gather tools and technics to reduce bandwith consumption during a sailing trip with sattelite communication (9kB/min).

This guide is mainly dedicated to OSX, but is is designed to give cross-plateform advice in the future

## Measuring

Measuring is the first step before regulating. Use the tool you have to diagnostic network consumption, like *Monitor* on *OSX*:

![](monitor.jpg)

## Use Lynx for webbrowing

[Lynx](http://lynx.browser.org) is a text based web browser picture and javascript free that allow reducing the bandwith when browsing the web.

- [ ] Tutorial needed

## Avoid DNS request

In order to reduce DNS request, there is two option:

- Using IP instead of name server => unfortunately, it doesn't work if you try to access a website using virtualhost
- Add common domain name to `/etc/hosts`. When looking for a domain name resolution, the system first look into this file to avoid DNS request

## Disable unnecessary services

- [ ] TODO: List unnecessary services

## Reducing picture size

Sending picture is generally a bad idea when you have a 9ko/min bitrate. If you really need to, you should definitely reduce the size and choose the jpeg format (if you don't need transparency). [ImageMagick](https://www.imagemagick.org) is a simple command line tool dedicated to that.

### Installation

    brew install imagemagick

### Usage

    $ convert -quality 60 monitor.png  -resize 1104x monitor.jpg

Look at the size I spared for the above image:

    $ ls -l monitor.*
-rw-r--r--@ 1 martin  staff    70K 29 jul 13:50 monitor.jpg
-rw-r--r--@ 1 martin  staff   496K 29 jul 13:48 monitor.png
