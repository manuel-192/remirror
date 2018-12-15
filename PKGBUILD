# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.34
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
  '3e866f0ed40c22299c927e3ba2735307623055e604dc61e24a144f8c475afef0cd025022a82a0a290ec0facf5f07668d7dac063953183d808b27bacbf109ce20'
  'a903e9db14b9e5e159d6a43b5e99218d4bf4ae7011edbf2337a5ccb885964e52803bb89c65f4785b31b8f14f8890cd21baca4feff7880fc0f83a9239e7f73aa8'
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
