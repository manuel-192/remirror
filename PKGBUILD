# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.49
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
  '0831e2145295a22fcb74d6270f63a28c4a0d34287e52bfa99b1e86d35cffc805b5efb6f76883df5635fd6ac5e58c58860e152f8abe8656d89690a074d3c25ff3'
  '29894ab77d49221782f1357f9204890dd824d2f21fad66045024b6f8c615fcaf5db44726c2d29367767c9671d5baa33fb82a345bf3a905831421e79e7251976e'
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
