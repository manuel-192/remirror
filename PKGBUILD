# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.33
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
  '9e32b311d3cb5388539d74c45574526c4b5a5e9bf9e83645c8a81d54c07148ce640f599d90e9068217141e85828eab6b5213fef1d3b89b46e74f48dd0a21e908'
  '48479ddcd4d710e46db49cb787d3ebb0a0a3963623e0a27a9f270dee65d745e7d8854805e9cd5f2934df6a8babd8250079d7013e6abbda02be607cc693099198'
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
