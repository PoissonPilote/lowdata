# lowdata

This repository is design to gather tools and technics to reduce bandwith consumption during a sailing trip with sattelite communication (9kB/min).

This guide is mainly dedicated to OSX, but is is designed to give cross-plateform advice in the future

## Use Lynx for webbrowing

[Lynx](http://lynx.browser.org) is a text based web browser picture and javascript free that allow reducing the bandwith when browsing the web.

- [ ] Tutorial needed

## Avoid DNS request

In order to reduce DNS request, there is two option:

- Using IP instead of name server => unfortunately, it doesn't work if you try to access a website using virtualhost
- Add common domain name to `/etc/hosts`. When looking for a domain name resolution, the system first look into this file to avoid DNS request

## Disable unnecessary services

- [ ] TODO: List unnecessary services
