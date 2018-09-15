# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.16
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
  '6fc28d945397b66cb3b7581ca01d8012ef976aacd0a3ba703c1bdd95a38735ee12197b38afc74aebf2a05b5de8c43016c4002297eee6f2900b1da045f572ce38'
  '0767c98c7377d7bf45eca259a503f7dcad2e28226d92c72da5d2cf88539a173160840316c602b6119a1d03af4aaa55d36841d477f23fb2f5dce9ba0beaf052e9'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
