# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.9
pkgrel=1
arch=('any')
license=('GPL')
depends=('bash' 'curl')
url="https://github.com/manuel-192/$pkgname"
source=(
  "$url/raw/master/$pkgname-$pkgver"
  "$url/raw/master/$pkgname-bash-completion"
)
sha512sums=(
  '535d97d331c7b5295cca11283c3eed549dc07b2aa6e2ed47672527a390f19eff5af8d6fe1e061d4afa146312d3611949c5b33d28e2c57566796b84ce78421eeb'
  'aa8c356937bfe1d2cd076d1baaa0bdc5c44c26119eee75d4e35857b344fee98a771547bddc9525dfb8ac20ef56f5fc49f2204d14d1bbd912383db1cc0c7b2f0c'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
