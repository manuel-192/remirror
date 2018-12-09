# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.27
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
  '1ba358d896db32065fc8e4d45962bf35b78c78d37eaffd590843b67b89abd114b64dee1d513b5817757dfcf071192eb308d8a3bccb49e85902fb070c9db783ff'
  '95b6c62eb81b92f61f2f8832c6e73728598d4d8939417334d266eb1052cd4b812d67a16ba01f8a4655c7ed447943f3e68ada4643ad1d7f7ecb9a533f1c2ed635'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
