# Maintainer: Krister Bäckman <ixevix@gmail.com>
# Contributor: Zhanibek Adilbekov <zhanibek.adilbekov@pm.me>
pkgname=slack-cli
pkgver=2.30.1
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

md5sums=('3c8493ba440fdbc7cf13b545f0cd0500')
