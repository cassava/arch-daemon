# Maintainer: Ben Morgan <benm.morgan@gmail.com>
pkgname=arch-daemon
pkgver=2.0
pkgrel=1
pkgdesc="Easily manipulate daemons in /etc/rc.d on Arch Linux"
arch=('any')
url="https://github.com/cassava/arch-daemon"
license=('ISC')
source=("https://github.com/downloads/cassava/$pkgname/$pkgname-$pkgver.tar.gz"
        "http://andrwe.org/doku.php/blog/scripting/bash/arch-daemon-completion?do=export_code&codeblock=0")

build() {
  cd $srcdir/$pkgname-$pkgver
  install -d ${pkgdir}/usr/bin/
  install -m755 daemon ${pkgdir}/usr/bin/daemon
  
  # install bash completion
  install -d ${pkgdir}/etc/bash_completion.d/
  install -m644 "${srcdir}/arch-daemon-completion?do=export_code&codeblock=0" ${pkgdir}/etc/bash_completion.d/arch-daemon

  # install zsh completion
  install -d ${pkgdir}/usr/share/zsh/site-functions
  install -m644 zsh-completion ${pkgdir}/usr/share/zsh/site-functions/arch-daemon
}

