# Maintainer: Brendan Hide <brendan at swiftspirit dot co dot za>
# Contributor: Brendan Hide <brendan at swiftspirit dot co dot za>
pkgname=systemd-journald-volatile
pkgver=0.1
pkgrel=3
pkgdesc="This tool automatically removes the journal folder on shutdown to prevent journald from storing to disk. System updates automatically recreate this folder, breaking expected behaviour. Journald has a similar option in journald.conf if preferred."
arch=("any")
url="http://swiftspirit.co.za/scripts/"
license=('GPL')
install=systemd-journald-volatile.install
depends=('systemd')

source=("systemd-journald-volatile-rm.sh"
        "systemd-journald-volatile.service")
md5sums=('0724a46941c56b5bb47e26d5e7013313'
         'daa987286c513e6aa03ad77f433c880f')

package() {

  mkdir -p ${pkgdir}/usr/lib/systemd/system ${pkgdir}/usr/bin/

  install -Dm0644 $srcdir/systemd-journald-volatile.service "${pkgdir}/usr/lib/systemd/system/"
  install -Dm0755 $srcdir/systemd-journald-volatile-rm.sh "${pkgdir}/usr/bin/"

}
#vim: set ft=PKGBUILD sw=2 ts=2 et
