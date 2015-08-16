# Maintainer: Alister Hood <Alister dot Hood at gmail dotcom>
pkgname=libguac-client-rdp
pkgver=0.7.4
pkgrel=1
pkgdesc="RDP client for the Guacamole web application"
arch=('i686' 'x86_64')
url="http://guacamole.sourceforge.net"
license=('GPL3')
depends=('libguac' 'freerdp')
makedepends=()
optdepends=()
provides=()
source=(http://sourceforge.net/projects/guacamole/files/current/source/$pkgname-$pkgver.tar.gz)
sha1sums=('8d23b00d1f16fbbd8b4948f0b32037618d9e3ae7')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
