# Maintainer: bgh <aur at bgh dot io>
# Contributor: Sylvain Durand <arch@durand.tf>

pkgname=uptime-kuma
pkgver=1.23.15
pkgrel=1
pkgdesc='A fancy self-hosted monitoring tool'

arch=('any')
url="https://github.com/louislam/${pkgname}"
license=('MIT')
depends=('nodejs')
makedepends=('npm')

source=(
  "${pkgname}-${pkgver}.tar.gz::${url}/archive/refs/tags/${pkgver}.tar.gz"
  "${pkgname}-dist-${pkgver}.tar.gz::${url}/releases/download/${pkgver}/dist.tar.gz"
  "uptime-kuma.service"
)
noextract=("${pkgname}-${pkgver}.tar.gz")

b2sums=('37bac888edb4182c27e117ad96ce19a1878487770ac8fcbb981e78babacb8083c964ef194e4360741fda3c7b9991fe52561c9abd8a8f94d4599390a94406891c'
        '3b703bdb82babd647caf4ce0283eeccaa36f7c5c27d3ccbbdd077efe5006b540741e657d42aac77cc8b3976e90ef4794f9b716dded60c2f4288908beca2c2089'
        'dbeac93f20082847cffc991224df2ac85963a03a02898b06b8444d4f33b2f4a51323bdcd2c940df41d1c8beed1e2b75fa449cff7d80dd9d5213f627bbe409f90')

package() {
  npm install --global --prefix "$pkgdir"/usr "$srcdir"/$pkgname-$pkgver.tar.gz --cache npm-cache

  cp --recursive "$srcdir"/dist "$pkgdir"/usr/lib/node_modules/$pkgname/
  install -D -m 644 "${srcdir}/uptime-kuma.service" ${pkgdir}/usr/lib/systemd/system/uptime-kuma.service
}
