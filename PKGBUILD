# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.18
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
  'eb678ed7ccaacbda4bd1df960b1857ab3e3d720afe9a334487c065dd87dab1299b9fc0edbff81e7ebe68f8479d9213dd2b7cac6ecdc297c8be0c7ccfce3c2e72'
  '0767c98c7377d7bf45eca259a503f7dcad2e28226d92c72da5d2cf88539a173160840316c602b6119a1d03af4aaa55d36841d477f23fb2f5dce9ba0beaf052e9'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
