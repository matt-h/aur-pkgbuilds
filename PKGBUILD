# Maintainer: Zhanibek Adilbekov <zhanibek.adilbekov@pm.me>
# Maintainer: Krister Bäckman <ixevix@gmail.com>
pkgname=slack-cli
pkgver=2.24.0
pkgrel=0
pkgdesc="Powerful Slack CLI via pure bash. Rich messaging, uploads, posts, piping, oh my!"
arch=('any')
url="https://api.slack.com/automation/quickstart"
license=('MIT')
depends=('bash')
source=(
	"https://downloads.slack-edge.com/slack-cli/slack_cli_""$pkgver""_linux_64-bit.tar.gz"
	)

package() {
	install -Dm755 "$srcdir/bin/slack" "$pkgdir/usr/bin/slack-cli"
}

md5sums=('98fcdb01a38bea57f73392cb2c8c4ce7')
