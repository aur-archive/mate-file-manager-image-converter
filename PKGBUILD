# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Giovanni "Talorno" Ricciardi <kar98k.sniper@gmail.com>
# Contributor: Xpander <xpander0@gmail.com>

pkgname=mate-file-manager-image-converter
pkgver=1.6.0
pkgrel=6
pkgdesc="A Caja extension for simple image conversions."
url="http://mate-desktop.org/"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('GPL')
depends=('gtk2' 'imagemagick' 'mate-file-manager')
makedepends=('mate-common' 'perl-xml-parser')
options=('!emptydirs')
groups=('mate-extra')
source=("http://pub.mate-desktop.org/releases/1.6/${pkgname}-${pkgver}.tar.xz")
sha1sums=('ab3b248e93f4c7322296d5856a8439d0a2515f53')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    ./autogen.sh \
        --prefix=/usr
    make
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
