---
author: Pascal Obry
date: 2023-02-21 01:00:00+00:00
layout: post
title: "darktable 4.2.1 released"
lede: dieppe.jpg
lede_author: Pascal Obry
tags:
  - announcement
  - darktable release
---

We're proud to announce the new bug fix release of darktable, 4.2.1!

The github release is here: [https://github.com/darktable-org/darktable/releases/tag/release-4.2.1](https://github.com/darktable-org/darktable/releases/tag/release-4.2.1).

As always, please don't use the autogenerated tarball provided by
github, but only our tar.xz file. The checksums are:

```
$ sha256sum darktable-4.2.1.tar.xz
603a39c6074291a601f7feb16ebb453fd0c5b02a6f5d3c7ab6db612eadc97bac  darktable-4.2.1.tar.xz
$ sha256sum darktable-4.2.1_arm64.dmg
d037a23e8b37f6971a1f2b7c4cf3e03647b168ad2fb43080761d7a307b43048d  darktable-4.2.1_arm64.dmg
$ sha256sum darktable-4.2.1_x86_64.dmg
993a29685397c6e1a429d84be578da9271eefc06d2c75c10818ffc00b7d04a00  darktable-4.2.1_x86_64.dmg
$ sha256sum darktable-4.2.1-win64.exe
31c4d6c522818eda87e48df44f267afd531339ef9d374fa02d44891e3755f7b5  darktable-4.2.1-win64.exe
```

When updating from the stable 4.0.x series, please bear in
mind that your edits will be preserved during this process, but the new
library and configuration will no longer be usable with 4.0.x.

You are strongly advised to take a backup first.

#### Important note: to make sure that darktable can keep on supporting the raw file format for your camera, *please* read [this post](https://discuss.pixls.us/t/raw-samples-wanted/5420?u=lebedevri) on how/what raw samples you can contribute to ensure that we have the *full* raw sample set for your camera under CC0 license!

Since darktable 4.2.0:

- Almost 300 commits to darktable+rawspeed
- 89 pull requests handled
- 18 issues closed

## The Big Ones

- N/A

## Other Changes

- JPEG files are identified using magic bytes instead of file
  extension. This helps in cases where JPEG images end up in
  files with unexpected extensions.

- Allow shortcuts to be assigned to the "quick access" style and preset
  menus at the bottom of the darkroom view

- Add a collapsible section to the sigmoid module so that
  controls not used in standard processing scenarios are hidden
  by default.

- Some minor modifications to image overlays in culling view to make
  them less intrusive.

## Bug Fixes

- Fix possible bad pinned memory transfer on OpenCL.

- Fix bug in date/time sanitization function that caused image capture
  timestamps to be corrupted when they contained a time zone with a
  negative offset.

- Fix toast messages containing "%".

- Fix collections module using exclude rules when the first filter is empty.

- Fix RGB curve histogram display when "compensate middle gray" is set.

- Fix possible infinite loop when a module fails to load.

- Properly honor "hide histogram" setting when restarting.

- Fix darktable-chart crash.

- Fix Y0 mask calculations in the demosaic module.

- Avoid using fscanf() for loading configuration to avoid broken Windows
  implementation.

- Add RYB vectorscope option to the darktable configuration file to
  ensure proper histogram view settings on startup.

- Ensure that wide popups are properly shown on the same display as
  the associated widget.

- Fix possible crash in camera tethering.

- Make yes/no buttons in dialog boxes respond to standard shortcuts
  <kbd>alt+y</kbd> and <kbd>alt+n</kbd>.

- Fix preferences sanitization, which was completely ineffective due to
  incorrect loading order.

- Add a link to the sigmoid module's online documentation.

- Fix tooltip on color calibration expander.

- Fix incorrect reporting of HEIF image bit depth, which resulted in
  incorrect color profile selection for images without embedded color
  profile data.

- Fix snapshot invalidation, which was too pessimistic and made
  switching snapshots slow.

- Fix some messages in LUT module.

## Lua

- N/A

## Notes

- N/A

## Changed Dependencies

- Update bundled LibRaw version to 0.21.1.

  For systems providing LibRaw 0.21.1 or newer, it is now possible to
  disable building the bundled copy by defining
  -DDONT\_USE\_INTERNAL\_LIBRAW=ON

### Mandatory

- Bump minimum required CMake version from 3.10 to 3.18.

### Optional

- Bump libheif minimum required version from 1.9.0 to 1.13.0.

- Relax libavif minimum required version from 0.9.1 back to 0.8.2.

## RawSpeed changes

- Massive Fuji decompressor refactoring, up to -25% less wall time
- Fuji GFX100(S): fix 16-bit sensor black/white levels
- Fix decoding of compressed Fuji raws with large filesize

## Camera support, compared to 4.2.0

### Base Support

- Canon EOS Kiss X10
- Canon EOS Kiss X10i
- Leica M9 (dng)
- Nikon Z 30 (12bit-compressed, 14bit-compressed)
- OM System OM-1
- OM System OM-5
- Panasonic DC-G95D (4:3)
- Panasonic DC-G99D (4:3)
- Ricoh GR IIIx (dng)

### Missing Compression Mode Support

- Fujifilm "non-lossless"/lossy
- Nikon high efficiency
- Sony lossless

### White Balance Presets

- Nikon Z 9

### Noise Profiles

- Fujifilm GFX100S
- Fujifilm X-H2
- Fujifilm X-H2S
- OM System OM-1
- Sony ILCE-7SM3
- Canon EOS 250D / Kiss X10 / Rebel SL3 / 200D Mark II
- Canon EOS R7

### Suspended Support

No samples on raw.pixls.us

- Creo/Leaf Aptus 22(LF3779)/Hasselblad H1
- Fujifilm FinePix S9600fd
- Fujifilm IS-1
- GoPro FUSION
- Kodak EasyShare Z980
- Leaf Aptus-II 5(LI300059)/Mamiya 645 AFD
- Leaf Credo 60
- Leaf Credo 80
- Minolta DiMAGE 5
- Olympus SP320
- Panasonic DMC-FX150
- Pentax Q10
- Phase One IQ250
- Samsung GX10
- Samsung GX20
- Samsung EK-GN120
- Samsung SM-G920F
- Samsung SM-G935F
- Sinar Hy6/ Sinarback eXact
- ST Micro STV680

## Translations

- German
- European Spanish
- Finnish
- French
- Hungarian
- Italian
- Japanese
- Dutch
- Polish
- Brazilian Portuguese
- Russian
- Slovenian
- Albanian
- Turkish (New)
- Ukrainian
- Chinese - Taiwan
