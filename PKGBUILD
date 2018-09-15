# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.13
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
  '01c81169eb9eee7438d8909abed6962c5be2dcd008d0e66791164170f7c949d68aae3366b46a51eada5e91579466a5bfb570cff5d7ceb25618a68c53872ead65'
  '42e4957bfe095a1def522c2d0726e95e8ca0c352c3f287b8f2b4c0d1efe8b168fc283b1577a5dfb8b0d1dfa85ae43ea645288746f0df8d355cce920c5c5ed396'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
