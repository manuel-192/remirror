# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.10
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
  '10cbf67a13cd5f83639964c2e4eabcd874cc0eb75aa751d01fb80d53b845a9d1cfc570c48e6901c5569302b2e04e0bbf1826f373592a17f14239d5259971adb7'
  'aa8c356937bfe1d2cd076d1baaa0bdc5c44c26119eee75d4e35857b344fee98a771547bddc9525dfb8ac20ef56f5fc49f2204d14d1bbd912383db1cc0c7b2f0c'
)

package() {
  cd $srcdir
  install -Dm755 $pkgname-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 $pkgname-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
}
