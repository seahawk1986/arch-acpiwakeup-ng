# Maintainer: Alexander Grothe <seahawk1986[at]hotmail.com>
pkgname=acpiwakeup-ng
pkgver=0.0.1
pkgrel=1
pkgdesc="set acpi wakeup times via dbus"
arch=('x86_64')
url="https://github.com/seahawk1986/acpiwakeup-ng"
license=('GPL')
depends=('python-gobject' 'python-dbus')
provides=('$pkgname')
backup=("etc/acpiwakeup.conf")
source=(git://github.com/seahawk1986/acpiwakeup-ng.git)
md5sums=('SKIP')


package() {
  cd $srcdir/$pkgname
  install -Dm755 acpiwakeup.py "$pkgdir/usr/bin/acpiwakeupd"
  install -Dm755 acpiwakeupctl "$pkgdir/usr/bin/acpiwakeupctl"
  install -Dm644 acpiwakeup.conf  "$pkgdir/etc/acpiwakeup.conf"
  install -Dm644 acpiwakeupd.service "${pkgdir}"/usr/lib/systemd/system/acpiwakeupd.service
}

# vim:set ts=2 sw=2 et:
