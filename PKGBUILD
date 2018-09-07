# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector'."
pkgver=0.1.4
pkgrel=1
arch=('any')
license=('GPL')
depends=('bash' 'curl')
url="https://github.com/manuel-192/remirror"
source=(
  "$url/raw/master/$pkgname-$pkgver"
)
sha512sums=(
  'd0031ca7e3fe7dcd1159f38ed2443d55c8d65d49e9a304a279167a9e4977019eead588714e386047aa410e3068b88e36d9389a6c6b1f551bccf8e730ef3a2162'
)

package() {
  cd $srcdir
  install -Dm555 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
}
