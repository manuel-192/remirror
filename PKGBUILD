# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.32
pkgrel=1
arch=('any')
license=('GPL')
depends=('bash' 'curl')
url="https://github.com/manuel-192/$pkgname"
source=(
  "$url/raw/master/${pkgname}-$pkgver"
  "$url/raw/master/${pkgname}-bash-completion"
  "$url/raw/master/${pkgname}.service"
  "$url/raw/master/${pkgname}.timer"
)
sha512sums=(
  '619bf42660f520a46f22991a1a7d2729b21f3ad6dd4480dfd0095fd728b6cc8ae3e9dd6307b67080f812498370000874d29e8f4f1971698727a16dfb25f52f32'
  '8edcc3ae19e5d8c401c430aa7b0d0bc665b4d7689118c9c15961968622d4d5e36fe2243550b33c3d7f802cae2e1a412282dcbbf14672006b4c28e063a6c0d1c7'
  '72a3aa1b551b9992dbbcc73e4f802767161fa7b60b12864d10288cf42f03f144306120518518d56f02d45dc1b5ff208c9a3cea5b24d155138d3aa6ce7c5ff1e1'
  'f90e757080ac298c1bb5c00d061e0a7019f1a74b28befa6967be6d284c311b4ffe5fc37fd4f4c530262c8cd918b3e1848e5eca145f496f48ef659a4ac6ec99db'
)

package() {
  cd $srcdir
  install -Dm755 ${pkgname}-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 ${pkgname}-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
  install -Dm644 ${pkgname}.timer           $pkgdir/etc/systemd/system/${pkgname}.timer
  install -Dm644 ${pkgname}.service         $pkgdir/etc/systemd/system/${pkgname}.service
}
