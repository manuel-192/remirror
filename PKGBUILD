# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.15
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
  '89f9683f923f3739386697af58eae64ec153c872278ba3ac0c7dac8da61541e139ab6bf67b240ba00644f37a8f7434dcf16b10943f11024f6c9f61ac8579445e'
  '0767c98c7377d7bf45eca259a503f7dcad2e28226d92c72da5d2cf88539a173160840316c602b6119a1d03af4aaa55d36841d477f23fb2f5dce9ba0beaf052e9'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
