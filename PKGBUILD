# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.22
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
  '6f06efc239596b2a6b98e944bce3eb77c98c02de199a934ed1df0a92e5d644aa254754402e806e9614e17483af3f12e894f10d316d9f5f72ae4a7b8e4e90c671'
  '8c64c10a69f16c9d91e7959b903b0cf7163997cf3bf73ab514b164ff9f322d3f4bf3b9ae6be453fb547fe0750874f27e064e5660a6bad111b4a9566e9ef3f1f7'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
