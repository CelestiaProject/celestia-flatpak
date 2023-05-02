Celestia Flatpak
================

This repository provides the necessary components to build and install a Flatpak of [Celestia][celestia]. This is not in any way associated with the Celestia project. I just made this for personal use.

Building and Installing
-----------------------

```bash
$ flatpak-builder build --user --install --force-clean space.celestia.celestia_qt6.yml
```

This may complain about missing dependencies. If it does, try running the following first:

```bash
$ flatpak-builder build --install-deps-only --install-deps-from=flathub space.celestia.celestia_qt6.yml
```

It also may give a cryptic error about "rofiles". If so, simply add the ` --disable-rofiles-fuse` option.

[celestia]: https://github.com/CelestiaProject/Celestia
