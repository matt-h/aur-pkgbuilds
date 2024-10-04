# Maintainer: Krister Bäckman <ixevix@gmail.com>
# Contributor: Zhanibek Adilbekov <zhanibek.adilbekov@pm.me>
pkgname=slack-cli
pkgver=2.29.2
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

md5sums=('b22e1f95add8e83ca9cdea55022adcdd')
