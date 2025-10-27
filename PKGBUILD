# Maintainer: Krister Bäckman <ixevix@gmail.com>
# Contributor: Zhanibek Adilbekov <zhanibek.adilbekov@pm.me>
pkgname=slack-cli
pkgver=3.9.0
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

md5sums=('eda4afbbf2a3fa022b4e6f1008b72eb7')
