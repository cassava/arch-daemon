# Contributor: Ben Morgan <benm.morgan@gmail.com>
pkgname=arch-daemon
pkgver=1.8
pkgrel=1
pkgdesc="arch-daemon manipulates daemons in /etc/rc.d on Arch Linux"
arch=('any')
url="https://github.com/cassava/arch-daemon"
license=('ISC')
groups=()
depends=()
makedepends=()
provides=()
conflicts=()
replaces=()
backup=()
source=(https://github.com/downloads/cassava/$pkgname/$pkgname-$pkgver.tar.gz)
noextract=()

build() {
  cd $srcdir/$pkgname-$pkgver
  install -d $pkgdir/usr/bin/
  install -m755 daemon $pkgdir/usr/bin/daemon
}
md5sums=('e8714641a5018fd7a6b69fce0ce34446')
