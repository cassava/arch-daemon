# Maintainer: Ben Morgan <benm.morgan@gmail.com>
pkgname=arch-daemon
pkgver=2.0b1
pkgrel=1
pkgdesc="Easily manipulate daemons in /etc/rc.d on Arch Linux"
arch=('any')
url="https://github.com/cassava/arch-daemon"
license=('ISC')
install=('arch-daemon.install')
source=("https://github.com/downloads/cassava/$pkgname/$pkgname-$pkgver.tar.gz"
        "http://andrwe.org/doku.php/blog/scripting/bash/arch-daemon-completion?do=export_code&codeblock=0")

build() {
  cd $srcdir/$pkgname-$pkgver
  install -d ${pkgdir}/usr/bin/
  install -m755 daemon ${pkgdir}/usr/bin/daemon
  
  # install bash completion
  install -d ${pkgdir}/etc/bash_completion.d/
  install -m644 "${srcdir}/arch-daemon-completion?do=export_code&codeblock=0" ${pkgdir}/etc/bash_completion.d/arch-daemon

  # install zsh completion (not complete)
  #install -d ${pkgdir}/usr/share/zsh/site-functions
  #install -m644 zsh-completion ${pkgdir}/usr/share/zsh/site-functions/arch-daemon
}

md5sums=('5f93670959d1dd4f3c01eaea3396e5a1'
         'd992807f4f980336a941402cca3f6936')
