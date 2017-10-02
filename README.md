# Arc Theme Wal

This is a fork of the Arc theme that is able to be colored by [pywal!](https://github.com/dylanaraps/pywal)

## Arc Wal is available in three variants 

##### Arc-Wal

![A screenshot of the Arc theme](http://i.imgur.com/Ph5ObOa.png)

##### Arc-Darker-Wal

![A screenshot of the Arc-Darker theme](http://i.imgur.com/NC6dqyl.png)

##### Arc-Dark-Wal

![A screenshot of the Arc-Dark theme](http://i.imgur.com/5AGlCnA.png)


### Installation

**Note:** After installation you will need to run [pywal](https://github.com/dylanaraps/pywal) for it to theme the colors.

To build the theme the follwing packages are required 
* `autoconf`
* `automake`
* `pkg-config` or `pkgconfig` for Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` to clone the source directory

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following
* GNOME Shell 3.14 - 3.24, GTK 3.14 - 3.22
* The `gnome-themes-standard` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

Clone the git repository with

    git clone https://github.com/kotajacob/arc-theme-wal --depth 1 && cd arc-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable Arc Light support
    --disable-darker           disable Arc Darker support
    --disable-dark             disable Arc Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support

    --with-gnome=<version>     build the theme for a specific GNOME version (3.14, 3.16, 3.18, 3.20, 3.22)
                               Note 1: Normally the correct version is detected automatically and this
                               option should not be needed.
                               Note 2: For GNOME 3.24, use --with-gnome-version=3.22
                               (this works for now, the build system will be improved in the future)

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `Arc-Wal`, `Arc-Darker-Wal` or `Arc-Dark-Wal` as Window/GTK+ theme and `Arc-Wal` or `Arc-Dark-Wal` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `Arc-Wal-solid`, `Arc-Darker-Wal-solid` and `Arc-Dark-Wal-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{Arc-Wal,Arc-Darker-Wal,Arc-Dark-Wal}

## License
Arc Theme Wal is available under the terms of the GPL-3.0. See `COPYING` for details.

## Full Preview
![A full screenshot of the Arc theme](http://i.imgur.com/tD1OBQ3.png)
<sub>Screenshot Details: Icons: [Arc](https://github.com/horst3180/arc-icon-theme) | Launcher Icons based on [White Pixel Icons](http://darkdawg.deviantart.com/art/White-Pixel-Icons-252310560) | [Wallpaper](https://pixabay.com/photo-869593/) | Font: Futura Bk bt</sub>
