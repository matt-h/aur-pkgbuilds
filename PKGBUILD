# Maintainer: Krister Bäckman <ixevix@gmail.com>
# Contributor: Zhanibek Adilbekov <zhanibek.adilbekov@pm.me>
pkgname=slack-cli
pkgver=3.0.0
pkgrel=0
pkgdesc="The Slack CLI is a set of tools critical to building workflow apps for Slack. Requires Deno."
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

md5sums=('107c5206394af9a94c1e7f66cfa3602b')
