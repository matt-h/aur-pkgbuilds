aur-pkgbuilds
=============

A collection of the PKGBUILDs I maintain for the [Arch Linux AUR](https://aur.archlinux.org)

Powered by [aurpublish](https://github.com/eli-schwartz/aurpublish)

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
All PKGBUILD files in this repository are licensed under the Unlicense.
