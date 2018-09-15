# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.17
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
  'cee73e3e039244bf5265479f780dafed6551c18d0c862f858fc8b874ee54a5091245a7b51476c6d8ca8ba74aaadd2598ed802819aa0ce0d8011c299fcb58b3fa'
  '0767c98c7377d7bf45eca259a503f7dcad2e28226d92c72da5d2cf88539a173160840316c602b6119a1d03af4aaa55d36841d477f23fb2f5dce9ba0beaf052e9'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
