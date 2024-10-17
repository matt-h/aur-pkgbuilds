# Maintainer:
# Contributor: Mattia Borda <mattiagiovanni.borda@icloud.com>

pkgname=furtherance
pkgver=1.8.3
pkgrel=1
pkgdesc="Track your time without being tracked"
arch=('x86_64')
url="https://github.com/lakoliu/Furtherance"
license=('GPL-3.0-or-later')
depends=('cairo'
         'dbus'
         'dconf'
         'gcc-libs'
         'gdk-pixbuf2'
         'glib2'
         'glibc'
         'graphene'
         'gtk4'
         'hicolor-icon-theme'
         'libadwaita'
         'pango'
         'sqlite')
makedepends=('cargo' 'meson')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/lakoliu/Furtherance/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('2cca9ab2c2b81c0d9ed94673fbf62b3a1ad11c813cd67038c8c5aeb7d87e37dc')

build() {
    arch-meson "${pkgname^}-${pkgver}" build
    meson compile -C build
}

package() {
    meson install -C build --destdir "${pkgdir}"
}
