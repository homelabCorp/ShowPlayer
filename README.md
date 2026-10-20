# ShowPlayer

Video and audio playback for live events, built on FFmpeg's libraries: a cue list with Mitti-style behaviour per cue,
a program output on a second display, and FFmpeg's format support. One app for Windows, macOS and Linux.

This repository holds ShowPlayer's releases: **[the latest release](https://github.com/homelabCorp/ShowPlayer/releases/latest)** has a package for each
platform, the source it was built from, and what is new in it.

## Installing

- **Windows**: `ShowPlayer-<version>-win-x64-setup.exe` installs the app; the `win-x64.zip` is the same build, to run
  from a folder with nothing installed. The build is not yet code-signed, so Windows says "Windows protected your PC"
  the first time: More info, then Run anyway.
- **macOS**: `ShowPlayer.app` for Apple silicon (the `osx-arm64` zip) or Intel (`osx-x64`), signed ad hoc, not
  notarised. Move it to Applications. Gatekeeper stops the first launch: on macOS 15 allow it in System Settings,
  Privacy & Security, Open Anyway; before 15, right-click the app and choose Open.
- **Linux**: unzip the `linux-x64` zip and run `ShowPlayer`.

## Updates

ShowPlayer looks for a newer release as it starts and every six hours, downloads it while no cue is on air, and offers
it in a banner in its main window. Nothing is installed until the operator clicks **Install and restart**, and never
with a cue on air. **Preferences > General** turns the looks off; **Check for Updates Now** looks at once. Each
release's `update.json` is signed, and a copy takes nothing whose signature or SHA-256 does not hold.

## Licence

ShowPlayer is free software under the GNU General Public License, version 2 or later; each release carries its source
as `ShowPlayer-<version>-source.tar.gz`. FFmpeg's libraries in it are under the GNU Lesser General Public License, and
their source is attached beside them. GitHub's own "Source code" archives of a release hold this repository alone.
