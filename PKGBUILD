# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.44
pkgrel=1
arch=('any')
license=('GPL')
depends=('bash' 'curl' 'pacman')
url="https://github.com/manuel-192/$pkgname"
source=(
  "$url/raw/master/${pkgname}-$pkgver"
  "$url/raw/master/${pkgname}-bash-completion"
  "$url/raw/master/${pkgname}.service"
  "$url/raw/master/${pkgname}.timer"
)
sha512sums=(
  '5a202699579ce86af6ef9101ea07f601ad3fccfd67627710f105a01daabd778f9285e702aac6085f9a8223d6d6041a989a10a1273db56907728a5789f07a720a'
  'bac3c0752bf8d40320c474ed4bf8448e8859f84c6a48ab7ead472def3425a8ae1015ac5df5c2a870bd0daca625ce50f72112125468287532b2431687921ca282'
  '73c10c7de62b776c711034765303757dd4c03797caecd2f4bab7691f146477f87dfe9fd1fbb5b1203e334ecee0b8454a96e26954d6aaff9b59cc9ce7c448dbbe'
  'f90e757080ac298c1bb5c00d061e0a7019f1a74b28befa6967be6d284c311b4ffe5fc37fd4f4c530262c8cd918b3e1848e5eca145f496f48ef659a4ac6ec99db'
)

package() {
  cd $srcdir
  install -Dm755 ${pkgname}-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 ${pkgname}-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
  install -Dm644 ${pkgname}.timer           $pkgdir/usr/lib/systemd/system/${pkgname}.timer
  install -Dm644 ${pkgname}.service         $pkgdir/usr/lib/systemd/system/${pkgname}.service
}
