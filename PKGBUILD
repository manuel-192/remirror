# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.38
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
  'd1a157f8795a0ef8bcddd482e7e719bab66c9593f9027d34cb49a8ad50c03a3152aa313698ab52ade732b0e6d3741efcdd43c2616651e8e03825ff807f2f00b1'
  '24150b8efeb079238855ca58baeafef86cb5f3c19d299bccf454b5a07f64940cf546f3984313209b1a1aee8ceb1713241e3bce4a536ba76db5ec6f9b63305890'
  '73c10c7de62b776c711034765303757dd4c03797caecd2f4bab7691f146477f87dfe9fd1fbb5b1203e334ecee0b8454a96e26954d6aaff9b59cc9ce7c448dbbe'
  'f90e757080ac298c1bb5c00d061e0a7019f1a74b28befa6967be6d284c311b4ffe5fc37fd4f4c530262c8cd918b3e1848e5eca145f496f48ef659a4ac6ec99db'
)

package() {
  cd $srcdir
  install -Dm755 ${pkgname}-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 ${pkgname}-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
  install -Dm644 ${pkgname}.timer           $pkgdir/etc/systemd/system/${pkgname}.timer
  install -Dm644 ${pkgname}.service         $pkgdir/etc/systemd/system/${pkgname}.service
}
