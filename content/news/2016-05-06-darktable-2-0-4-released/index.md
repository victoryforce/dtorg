---
author: houz
comments: true
date: 2016-05-06 11:15:19+00:00
layout: post
link: /2016/05/darktable-2-0-4-released/
slug: darktable-2-0-4-released
title: darktable 2.0.4 released
lede: mairi_wide.jpg
lede_author: <a href="https://houz.org/">houz</a>
wordpress_id: 4059
tags:
  - announcement
  - darktable release
---
we're proud to announce the fourth bugfix release for the 2.0 series of darktable, 2.0.4!

the github release is here: [https://github.com/darktable-org/darktable/releases/tag/release-2.0.4](https://github.com/darktable-org/darktable/releases/tag/release-2.0.4).

as always, please don't use the autogenerated tarball provided by github, but only our tar.xz. the checksum is:

    $ sha256sum darktable-2.0.4.tar.xz
    80e448622ff060bca1d64bf6151c27de34dea8fe6b7ddb708e1e3526a5961e62  darktable-2.0.4.tar.xz
    $ sha256sum darktable-2.0.4.dmg
    1e6306f623c3743fabe88312d34376feae94480eb5a38858f21751da04ac4550  darktable-2.0.4.dmg

and the changelog as compared to 2.0.3 can be found below.

## New Features

* Support grayscale input profiles
* Add a BRG profile for testing purposes

## Bugfixes

* Fix the GUI with GTK 3.20
* Fix the color profiles we ship
* Fix two deflicker (exposure iop, mode = automatic) issues
* Fix trashing of files on OSX
* Fix Rights field in Lua

## Base Support

* Nikon D5
* Sony ILCA-68

## White Balance Presets

* Pentax K-S1
* Sony ILCA-68

## Noise Profiles

* Canon PowerShot G15
* Fujifilm X70
* Olympus PEN-F
* Panasonic DMC-GF7

## Translation Added

* Slovenian

## Translations Updates

* Catalan
* Dutch
* German
* Hebrew
* Slovak
* Spanish
