# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.20
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
  '99a1f135b1ac1284a76309996486f243d9fdba59442c310637dd5bc24ff6d37bcd5099b9652ab11bedab98e7e6a088f05dd5c973fcfe7a5fd89ec2b88fd3e254'
  '8c64c10a69f16c9d91e7959b903b0cf7163997cf3bf73ab514b164ff9f322d3f4bf3b9ae6be453fb547fe0750874f27e064e5660a6bad111b4a9566e9ef3f1f7'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
