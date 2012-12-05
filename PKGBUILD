# Maintainer: Maintainer: Matt Harrison < matt at mistbyte dot com >
# Contributor: Muhammad Qadri <Muhammad dot A dot Qadri at gmail dot com>
# This PKGBUILD is maintained at https://github.com/matt-h/voxforge-am-julius

pkgname=voxforge-am-julius
pkgver=2011.07.21
pkgrel=1
pkgdesc="Acoustic model information for use with Julius voice recognition software"
arch=('any')
url="http://www.voxforge.org/"
license=('GPL')
install=voxforge-am-julius.install
source=(http://www.repository.voxforge1.org/downloads/Nightly_Builds/AcousticModel-2011-07-21/Julius-3.5.2-Quickstart-Linux_AcousticModel-2011-07-21.tgz)
sha1sums=('ab1cf9df020f2b0b495e88049885ece15660e014')

build() {
  cd "$srcdir"

  install -D julian.jconf $pkgdir/usr/share/voxforge/julius/julian.jconf
  install -d $pkgdir/usr/share/voxforge/julius/grammar/
  install -t $pkgdir/usr/share/voxforge/julius/grammar/ grammar/*
  install -d $pkgdir/usr/share/voxforge/julius/acoustic_model_files/
  install -t $pkgdir/usr/share/voxforge/julius/acoustic_model_files/ acoustic_model_files/*
}

# vim:set ts=2 sw=2 et:
