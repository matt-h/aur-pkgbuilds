# Maintainer: bgh <aur at bgh dot io>
# Contributor: Sylvain Durand <arch@durand.tf>

pkgname=uptime-kuma
pkgver=1.23.16
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

b2sums=('7ba8eeabe61dfb2aea46c3b9ed53c97adaed36f00ae8ecd3329cab5db205790cbac97ed3fa728d3fdb9630479dff910c370c8cbd9eb4f4a676bb6533ada5ad27'
        '45e58f59f1562a21aee840fb7adb108b64f4a09c8c739e7847b348c8845cdbca5d0d70035fc4229c1a622589241eebdeae41b56a3669162c004e5aa665e94e40'
        'dbeac93f20082847cffc991224df2ac85963a03a02898b06b8444d4f33b2f4a51323bdcd2c940df41d1c8beed1e2b75fa449cff7d80dd9d5213f627bbe409f90')

package() {
  npm install --global --prefix "$pkgdir"/usr "$srcdir"/$pkgname-$pkgver.tar.gz --cache npm-cache

  cp --recursive "$srcdir"/dist "$pkgdir"/usr/lib/node_modules/$pkgname/
  install -D -m 644 "${srcdir}/uptime-kuma.service" ${pkgdir}/usr/lib/systemd/system/uptime-kuma.service
}
