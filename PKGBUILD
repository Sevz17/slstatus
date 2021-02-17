# Maintainer: Leonardo Hernández <leohdz172@outlook.com>
pkgname=slstatus
pkgver=0
pkgrel=1
pkgdesc="A status monitor for window managers that use WM_NAME or stdin to fill the status bar"
arch=('x86_64')
url="https://github.com/Sevz17/slstatus.git"
license=('ISC')
source=("$pkgname-$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  make
}

package() {
  cd "$srcdir/$pkgname"
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}
