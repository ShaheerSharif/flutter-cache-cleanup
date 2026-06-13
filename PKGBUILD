pkgname=flutter-cache-cleanup
pkgver=1.0.0
pkgrel=1
pkgdesc="Pacman hook to cleanup flutter-bin cache and FUSE mounts"
arch=('any')
license=('MIT')

depends=(
  'fuse3'
  'util-linux'
)

optdepends=(
  'flutter-bin: package whose cache is cleaned by this hook'
)

package() {
  install -Dm755 flutter-cache-cleanup \
    "$pkgdir/usr/local/bin/flutter-cache-cleanup"

  install -Dm644 flutter-cache-cleanup.hook \
    "$pkgdir/usr/share/libalpm/hooks/zz-flutter-cache-cleanup.hook"
}
