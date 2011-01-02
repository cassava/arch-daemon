# Maintainer: Ben Morgan <benm.morgan@gmail.com>
pkgname=arch-daemon
pkgver=1.9
pkgrel=1
pkgdesc="arch-daemon manipulates daemons in /etc/rc.d on Arch Linux"
arch=('any')
url="https://github.com/cassava/arch-daemon"
license=('ISC')
source=(https://github.com/downloads/cassava/$pkgname/$pkgname-$pkgver.tar.gz)

build() {
  cd $srcdir/$pkgname-$pkgver
  install -d $pkgdir/usr/bin/
  install -m755 daemon $pkgdir/usr/bin/daemon
  
  # install bash completion
  install -d $pkgdir/etc/bash_completion.d
  install -m644 bash-completion $pkgdir/etc/bash_completion.d/arch-daemon

  # install zsh completion
  install -d $pkgdir/usr/share/zsh/site-functions
  install -m644 zsh-completion $pkgdir/usr/share/zsh/site-functions/arch-daemon
}
