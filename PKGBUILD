# Maintainer: Matt Harrison <matt@mistbyte.com>

pkgname=bitcasa
pkgver=0.9.2.50
pkgrel=1
pkgdebrel=1
pkgdesc="Infinite Storage in the cloud"
arch=('x86_64')
url="http://www.bitcasa.com"
license=('custom')
depends=('boost-libs' 'protobuf')
makedepends=('binutils' 'tar')
source=(
    "http://dist.bitcasa.com/release/ubuntu/pool/main/b/bitcasa/bitcasa_${pkgver}_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/c/curl/libcurl3_7.22.0-3ubuntu4_amd64.deb"
    "http://security.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.0.0_1.0.1-4ubuntu5.2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/o/openldap/libldap-2.4-2_2.4.28-1.1ubuntu4_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libgssapi3-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libheimntlm0-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libasn1-8-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libhcrypto4-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libroken18-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/c/cyrus-sasl2/libsasl2-2_2.1.25.dfsg1-3_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libkrb5-26-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "http://mirrors.rit.edu/ubuntu/pool/main/h/heimdal/libwind0-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb"
    "bitcasa")
sha256sums=(
    '693ae882c1658d47ab0aafd328b1f4f6c68a52639ea78fcc9e4734505dd5f922'
    '46d58ee60211b8467f6e237d194e0919dc9ea7a49bc15e963b212899a4e5d990'
    'e3c5c6d669d3ae02bea0cfeb60b24435eed12189dbdabac17c980144cf36a803'
    '024df6e175efc8747454a4ca873598c16bc02eab6b811d418e78a5038b39dc09'
    'cfa2e6119d5148a0c09e1b0407b32b121ee0dcbf73ac39e9522a6efce19b4197'
    '9c37b58b280f781cd3494626cab569672e10777cd4200c1bbd814ebe3ac84269'
    '480ef08a0e86c73f60d89dd3fc1c601712cafe65663428ac3850c5a43de928aa'
    '8bda824f525937657e24246ac91bb6374c2924ba816b94c9bb040e73a8172c60'
    'eb6b9525307eafd759949e891179eda529ae75d1e0c248cc06d6aad937224a6d'
    '7ee06d0eb0075b3ca01a162c844984675084bc861a03ce84b0803949ef8c799c'
    '3c3dc5a53b8d3556c8d925aab9ff101e6c149e3794efb55faddb26a62a55f1bd'
    '6dd9066a234bc4d99df6f1c2b625fc8d86b8e85e8571cd376f521040fef76c8e'
    '634ee5a5618256f61a9c1316ccb8270cfd201161ea2a91a55fb3523939d6a695'
)

build() {
	install -d "$pkgdir/opt/bitcasa"
	cd $srcdir/
	ar -p bitcasa_${pkgver}_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
    cp "$srcdir/usr/bin/Bitcasa" "$pkgdir/opt/bitcasa/"
    cp "$srcdir/bitcasa" "$pkgdir/opt/bitcasa/bitcasa"
    chmod 755 "$pkgdir/opt/bitcasa/Bitcasa"
	chmod 755 "$pkgdir/opt/bitcasa/bitcasa"
    install -d "$pkgdir/usr/bin"
    
	ln -s "/opt/bitcasa/bitcasa" "$pkgdir/usr/bin/bitcasa"
	ln -s "/opt/bitcasa/bitcasa" "$pkgdir/usr/bin/Bitcasa"
	
	# extract libs from ubuntu package
	ar -p libcurl3_7.22.0-3ubuntu4_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libssl1.0.0_1.0.1-4ubuntu5.2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libldap-2.4-2_2.4.28-1.1ubuntu4_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libgssapi3-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libheimntlm0-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libasn1-8-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libhcrypto4-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libroken18-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libsasl2-2_2.1.25.dfsg1-3_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libkrb5-26-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
	ar -p libwind0-heimdal_1.6~git20120311.dfsg.1-2_amd64.deb data.tar.gz | tar zxf - -C "${srcdir}" || return 1
    
    # copy libs to the lib folder
    cp -R "$srcdir/usr/lib/x86_64-linux-gnu" "$pkgdir/opt/bitcasa/lib"
    cp -R "$srcdir/lib/x86_64-linux-gnu/" "$pkgdir/opt/bitcasa/lib/"

	# link libs needed
	ln -s /usr/lib/libboost_regex.so $pkgdir/opt/bitcasa/lib/libboost_regex.so.1.46.1
	ln -s /usr/lib/libboost_filesystem.so $pkgdir/opt/bitcasa/lib/libboost_filesystem.so.1.46.1
	ln -s /usr/lib/libboost_thread.so $pkgdir/opt/bitcasa/lib/libboost_thread.so.1.46.1
	ln -s /usr/lib/libboost_system.so $pkgdir/opt/bitcasa/lib/libboost_system.so.1.46.1
	ln -s /usr/lib/liblog4cpp.so $pkgdir/opt/bitcasa/lib/liblog4cxx.so.10
	ln -s /usr/lib/libgnutls.so $pkgdir/opt/bitcasa/lib/libgnutls.so.26
}
