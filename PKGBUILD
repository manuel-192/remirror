# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgver=0.1
pkgrel=1
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector'."
arch=('any')
license=('GPL')
depends=('bash' 'curl')
url="https://github.com/manuel-192/remirror"
source=(
  "$url/raw/master/$pkgname-$pkgver"
)
sha512sums=(
  '5825aa4bf273bbd6e53c9c604f10ee6c09ede6dcce5bff5f8d854f1e255f3f373ee60e77e9e4950f953b75376c36287c1d395cb962a2aead08ef671edf13767d'
)

package() {
  cd $srcdir
  install -Dm555 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
}
