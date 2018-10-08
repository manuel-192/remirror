# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.23
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
  'e21da7122f3b2a3ab1a3385ee82a7cf7edc1480cc216fd0e29ed43c4105b5bb47751e9ae491baa432e0297b4fd229272c5fff34948bbf327a1aaa25a16d77f03'
  '8c64c10a69f16c9d91e7959b903b0cf7163997cf3bf73ab514b164ff9f322d3f4bf3b9ae6be453fb547fe0750874f27e064e5660a6bad111b4a9566e9ef3f1f7'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
