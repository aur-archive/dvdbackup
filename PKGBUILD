# Maintainer: yugrotavele <yugrotavele at archlinux dot us>
# Contributor: Varun Acharya <varun@archlinux.org>
# Contributor: Nicolai Lissner <nlissne@linux01.gwdg.de>

pkgname=dvdbackup
pkgver=0.4.2
pkgrel=1
pkgdesc="A tool to rip video DVDs from the command line"
arch=('i686' 'x86_64')
url="http://dvdbackup.sourceforge.net/"
license=('GPL')
depends=('libdvdread')
optdepends=('libdvdcss: to decrypt encrypted dvds')
source=("http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.xz")
md5sums=('28f273b2f27a3afea3a3c965ddbede86')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}
