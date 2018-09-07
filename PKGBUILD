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
  '531a12af8238d923a551e9c912d7eb3f5865cddbfe4df78c684f59ab699ba12c1002913ba2ebd80e96b670120cf422d245dd818453dc67b3a9059d2fc69c6d27'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
