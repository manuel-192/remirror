# Maintainer: manuel (see forum.antergos.com)

pkgname=remirror
pkgdesc="Ranks Antergos and Arch mirrors, somewhat resembles 'reflector', and replaces reflector-antergos."
pkgver=0.1.29
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
  '16d18a5621bb86527ea6f03c46cffd576a469cfc51d1a51efa54c236e994e96f945a80069a99e64526b0397dcd0fb8e1a609e923939bc23e3e786524f4cce791'
  '95b6c62eb81b92f61f2f8832c6e73728598d4d8939417334d266eb1052cd4b812d67a16ba01f8a4655c7ed447943f3e68ada4643ad1d7f7ecb9a533f1c2ed635'
  'fafce12f7297fcb622be2ff1062a7cadb49ab5266743617ca5d546f9a15756e6b2d6d434c6f9ad4904b5443da2cdcfb8b008a8b75868f30ea0cf8ca86621e15d'
  'f90e757080ac298c1bb5c00d061e0a7019f1a74b28befa6967be6d284c311b4ffe5fc37fd4f4c530262c8cd918b3e1848e5eca145f496f48ef659a4ac6ec99db'
)

package() {
  cd $srcdir
  install -Dm755 ${pkgname}-$pkgver $pkgdir/usr/bin/$pkgname
  install -Dm644 ${pkgname}-bash-completion $pkgdir/usr/share/bash-completion/completions/$pkgname
  install -Dm644 ${pkgname}.timer           $pkgdir/etc/systemd/system/${pkgname}.timer
  install -Dm644 ${pkgname}.service         $pkgdir/etc/systemd/system/${pkgname}.service
}
