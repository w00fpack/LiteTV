# Overview
[![screenshot](https://raw.githubusercontent.com/w00fpack/LiteTV/main/screenshots/LiteTV.webp)](https://raw.githubusercontent.com/w00fpack/LiteTV/main/screenshots/LiteTV.webp)

LiteTV is a small app that allows you to list, play, buffer and record TV on linux systems that hav a TV tuner adapter.  LiteTV is lightweight on resources requiring very little dependencies and/or libraries.

This sofware is currently being developed, so is at Alpha level.
- [ ] episode guide
- [ ] scheduled recording
- [ ] CI/CD

## Add-on Requirements
* A relatively new Linux kernel that supports DVB for the TV tune card that you have , is required.
* w_scan is needed to scan and store TV channels that you tuner finds
* [Yad](https://github.com/v1cont/yad) - GUIs
* mpv - TV display
*  [Streamsave](https://github.com/Sagnac/streamsave ) mpv plug-in - Recording (optional)

# Installation

 Download source and do a command similar to the following:

`cp -r src/* /`


# Quickstart

1.  Backup your ~/.config/mpv/channels.conf file (if you have one)
2.  Access your TV tuner hardware, and create a channels.conf file listing received TV channels.  This can be accomplished using the GUI<br />
	/usr/share/LiteTV/channels_add
3.  or manually via a command similar to the following<br />
	w_scan -ft -c US -M > ~/.config/mpv/channels.conf
4.  If wanted, edit ~/.config/mpv/channels.conf to add/remove/modify channels and there names.
5.  Run /bin/litetv

You can change a station icon by adding, and naming icons under /usr/share/LiteTV

## Playing and recording
While watching a channel, use the left and right arrows to jump in time.  The spacebar will pause the video.  Ctrl-Z starts recording, and Ctrl-X stops.

## Warnings
The video replay buffer as well as video recording take up a lot of disk space. This is because most TV is transmitted uncompressed.  Expect an hour long recording to take over 4GB of space.

# Documentation

The [GitHub Wiki](https://github.com/w00fpack/LiteTV/wiki) can serve as a central hub for all of
documentation, if there is a demand for this add-on, or if such is requested by the public.  This has not been done at this time, since Blender has an add-on section on it's website (which might be used). Possible Quick links:

* [Install](https://github.com/w00fpack/LiteTV/wiki/Installation)
* [Configure](https://github.com/w00fpack/LiteTV/wiki/Configuration-Settings)
* [Frequently Asked Questions](https://github.com/w00fpack/LiteTV/wiki/FAQ)

# License

This add-on is CC0 [licensed](https://github.com/w00fpack/LiteTV/LICENSE).  When applicable, this license is superceded by Blender's licensing.

# Contributing

To submit code changes, please open pull requests against [the GitHub repository](https://github.com/w00fpack/LiteTV/edit/master/README.md). Patches submitted in issues, email, or elsewhere will likely be ignored. Here's some general guidelines when submitting PRs:

 * In your pull request, please:
   * Describe the changes, why they were necessary, etc
   * Describe how the changes affect existing behaviour
   * Describe how you tested and validated your changes
   * Include any relevant screenshots/evidence demonstrating that the changes work and have been tested

[wiki]: https://github.com/w00fpack/LiteTV/wiki
