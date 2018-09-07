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
  '2f3b3b1e59eece392854dcab8f1365474ccb48fd02f5e0234890d262bd68bf28bfd2aa27e82cc48f29d559c6122178cf1bd9887c5f02189f601132b69dfaac53'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
