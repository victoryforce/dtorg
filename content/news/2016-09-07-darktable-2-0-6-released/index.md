---
author: houz
comments: true
date: 2016-09-07 17:44:52+00:00
layout: post
link: /2016/09/darktable-2-0-6-released/
slug: darktable-2-0-6-released
title: darktable 2.0.6 released
lede: spider_wide.jpg
lede_author: <a href="https://www.flickr.com/photos/andabata">Kees Guequierre</a>
wordpress_id: 4226
tags:
  - announcement
  - darktable release
---
we're proud to announce the sixth bugfix release for the 2.0 series of darktable, 2.0.6!

the github release is here: [https://github.com/darktable-org/darktable/releases/tag/release-2.0.6](https://github.com/darktable-org/darktable/releases/tag/release-2.0.6).

as always, please don't use the autogenerated tarball provided by github, but only our tar.xz. the checksum is:

    2368c1865221032061645342ba8c00bcd6d224e9829a55bc610e6cb67de738c1  darktable-2.0.6.tar.xz
    8376ab1bb74f4a25998ff1a7f03c8498b57064bf27700c9af53a7356e5a2ee1e  darktable-2.0.6.dmg

and the changelog as compared to 2.0.5 can be found below.

## New Features

* Jpeg format writer: use libexiv2 to write metadata, like with other formats
* Accept non-mosaiced raw files with 4 channels, assume they are RGBA (alpha channel is ignored)

## Bugfixes

* Once again, fix for yet another gtk theming regression...
* OpenCL: properly discard CPU-based OpenCL devices. Fixes crashes on startup with some broken OpenCL implementations like pocl.
* darktable-cli: do not even try to open display, we don't need it.
* Rawspeed: NikonDecoder: stop accepting generic camera entries. Fixes multitude of Nikon raw loading issues.
* OpenCL: fix border handling in crop&rotate module
* Hotpixels iop: make it actually work for X-Trans
* Clipping IOP: scale width of gray crop path with zoom level
* One more fixup to canon lens name reading from exif
* Fixup Bayer pattern for Olympus SP570UZ
* Fix internal build issue: do not assume that Perl's @INC contains '.'

## Base Support

* Canon EOS-1D X Mark II
* Canon EOS 1300D
* Canon EOS Kiss X80
* Canon EOS Rebel T6
* Canon EOS M10
* Canon PowerShot G7 X Mark II
* Canon PowerShot G9 X
* Fujifilm X-T2
* GITUP GIT2 action camera
* Panasonic DMC-FZ18 (16:9, 3:2)
* Panasonic DMC-FZ50 (16:9, 3:2)
* Pentax K-1
* Sony DSLR-A380
* Sony ILCE-6300
* Nikon D500
* Some other whitelevel fixups for some other Nikon cameras (in particular, mostly for 12-bit and not compressed raws)

## White Balance Presets

* Canon EOS-1D X Mark II
* Canon EOS 1300D
* Canon EOS Kiss X80
* Canon EOS Rebel T6
* Canon EOS M10
* Canon PowerShot G7 X Mark II
* Fujifilm X-T10
* Sony ILCE-6300

## Translations Updates

* Slovak
