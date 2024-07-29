# Maintainer: Krister Bäckman <ixevix@gmail.com>
# Contributor: Zhanibek Adilbekov <zhanibek.adilbekov@pm.me>
pkgname=slack-cli
pkgver=2.28.0
pkgrel=0
pkgdesc="Powerful Slack CLI via pure bash. Rich messaging, uploads, posts, piping, oh my!"
arch=('any')
url="https://api.slack.com/automation/quickstart"
license=('MIT')
depends=('git' 'deno')
source=(
	"https://downloads.slack-edge.com/slack-cli/slack_cli_""$pkgver""_linux_64-bit.tar.gz"
	)

package() {
	install -Dm755 "$srcdir/bin/slack" "$pkgdir/usr/bin/slack-cli"
}

md5sums=('50f63646daf7a547f2f9f5d204bff867')
