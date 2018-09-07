# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.5
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
  '905c90acb94e01ca5e4216a8fa0a78a33da0143789f950641a687cb9edee08714c4931c04d50d52a6e60ce29ccc970aa51e560368bbfd0eb193fc110380b39df'
  '05cf9ba265d31968f9a048e692a36cf841221b78d7afc36ee39ae616de6a5de5bb0f3865e2b335f70b0fe02a0aa5aeb3e5886db51951296cebfcf92938c73be6'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
