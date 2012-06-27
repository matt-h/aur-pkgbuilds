# $Id$
# Maintainer: Sagar Chalise <chalisesagar@gmail.com>
pkgname=geany-zencoding
pkgver=0.21
pkgrel=2
pkgdesc="Zen Coding plugin for geany"
arch=('x86_64' 'i686')
url="https://github.com/codebrainz/geany-zencoding"
license=('GPL2')
depends=('geany' 'python2')
makedepends=('intltool')
source=("https://github.com/codebrainz/geany-zencoding/tarball/51334a0259d48a972290dba4c471e1c1aa234931" "geany-zencoding.patch")
md5sums=('72a0bb7d67aa459cda625c5407bbcca3'
         '010252ba0d88a4d1ab820942c1b23f44')

build() {
  cd "$srcdir/codebrainz-geany-zencoding-51334a0/"
  patch -p1 -i ../geany-zencoding.patch
  ./autogen.sh
  ./configure --prefix=`pkg-config --variable=prefix geany`
  make
}

package() {
  cd "$srcdir/codebrainz-geany-zencoding-51334a0/"
  make DESTDIR="$pkgdir" install
}
