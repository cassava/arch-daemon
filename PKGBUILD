# Contributor: Ben Morgan <benm.morgan@gmail.com>
pkgname=arch-daemon
pkgver=1.7
pkgrel=1
pkgdesc="arch-daemon manipulates services or daemons on Arch Linux"
arch=('any')
url="https://github.com/cassava/arch-daemon"
license=('GPL')
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
md5sums=('a24e3e54c6f409105c3c9efefe0bf713')
