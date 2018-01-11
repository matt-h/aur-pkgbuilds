aur-pkgbuilds
=============

A collection of the PKGBUILDs I maintain for the [Arch Linux AUR](https://aur.archlinux.org)

Tools to manage this are copied from https://github.com/eli-schwartz/pkgbuilds

## How it works
Commit PKGBUILDs in named subdirectories. Export them to the AUR with the included `aurpublish` script, using the subtree push stratagem.
This preserves an independent history for third-party hosting, pull requests... ;)

## Commands
* `./setup.sh ssh`
> Append ssh-config rules for accessing the AUR.

* `./setup.sh hooks`
> Install [githooks](#hooks).

* `./aurpublish PACKAGE`
> Push PACKAGE to the AUR. With "--speedup", merges the split history back in.

* `./aurpublish -p PACKAGE`
> Pull package from the AUR (if you adopted an existing package, or have a co-maintainer).

* `./aurpublish log PACKAGE`
> View the git log of a package subtree.

## Copyright
All PKGBUILD files in this repository are licensed under the Unlicense

The helper scripts (aurpublish, *.sh, *.hook) used are licensed under the GPLv2 or (at your option) any later version by [eli-schwartz](https://github.com/eli-schwartz/pkgbuilds)
