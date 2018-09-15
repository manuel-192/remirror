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
  '2f3b3b1e59eece392854dcab8f1365474ccb48fd02f5e0234890d262bd68bf28bfd2aa27e82cc48f29d559c6122178cf1bd9887c5f02189f601132b69dfaac53'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
