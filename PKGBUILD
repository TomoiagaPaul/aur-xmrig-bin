# Maintainer: Hans-Nikolai Viessmann <hv15 AT hw.ac.uk>
_pkgname=xmrig
pkgname=${_pkgname}-bin
pkgver=2.4.4
pkgrel=1
pkgdesc="Monero cryptocurrency CPU miner, HTTP API disabled"
arch=('x86_64')
url="https://github.com/xmrig/xmrig"
license=('GPL')
depends=('glibc')
optdepends=('monero: wallet')
install=${_pkgname}.install
changelog=CHANGELOG.md
source=("https://github.com/xmrig/${_pkgname}/releases/download/v${pkgver}/${_pkgname}-${pkgver}-gcc7-xenial-amd64-no-api.tar.gz"
        "https://raw.githubusercontent.com/xmrig/xmrig/v${pkgver}/README.md")
md5sums=('964fbc0ee038cd3c0bf99ac7629ad053'
         'fd2b9292d4a69bbc42b506fc276e9ea2')

package() {
	cd "${_pkgname}-$pkgver"

    install -Dm755 xmrig "${pkgdir}/usr/bin/xmrig"
    install -Dm644 config.json "${pkgdir}/usr/share/doc/xmrig/config.json.example"
    install -Dm644 "${srcdir}/README.md" "${pkgdir}/usr/share/doc/xmrig/README.md"
}
