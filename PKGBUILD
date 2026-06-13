pkgname=flutter-cache-cleanup
_pkgname=flutter-cache-cleanup
pkgver=1.0.0
pkgrel=1
pkgdesc="Pacman hook to cleanup flutter-bin cache and FUSE mounts"
arch=('any')
license=('MIT')

source=(
  "${_pkgname}"
  "${_pkgname}.hook"
)

depends=(
  'fuse3'
  'util-linux'
)

optdepends=(
  'flutter-bin: package whose cache is cleaned by this hook'
)

package() {
  install -Dm755 "$srcdir/${_pkgname}" \
    "$pkgdir/usr/bin/${_pkgname}"

  install -Dm644 "$srcdir/${_pkgname}.hook" \
    "$pkgdir/usr/share/libalpm/hooks/${_pkgname}.hook"
}

sha256sums=('accee40ecc650276021b6f108700e4f5a4869791e766d86e03e52f861d43b82d'
            '7c50d2a7d095753a53e504cfedcdef19db6f584463d117fc51258313edcf717d')
