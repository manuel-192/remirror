# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.6
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
  '109f2819494f227afbada80d2c7dd5059db4c451663146afe36e28f33db90e05647fae5029fd2b8a84de6940ec25ff1918dcf40de3a6a914993cc34e3b992602'
  '531a12af8238d923a551e9c912d7eb3f5865cddbfe4df78c684f59ab699ba12c1002913ba2ebd80e96b670120cf422d245dd818453dc67b3a9059d2fc69c6d27'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
