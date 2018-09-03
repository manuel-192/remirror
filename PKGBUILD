# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector'."
pkgver=0.2
pkgrel=1
arch=('any')
license=('GPL')
depends=('bash' 'curl')
url="https://github.com/manuel-192/remirror"
source=(
  "$url/raw/master/$pkgname-$pkgver"
)
sha512sums=(
  '7115d51839e5fa1bd22027582af1731a0b4a5183a255cacdf04274efeb83372f931f9f84275a52b1c09edf18dc2bec12be17a81c6e59860c4d7857e2eac9c7c4'
)

package() {
  cd $srcdir
  install -Dm555 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
}
