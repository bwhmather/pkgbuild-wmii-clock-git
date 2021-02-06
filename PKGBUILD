# Maintainer: Ben Mather <bwhmather@bwhmather.com>

pkgname=wmii-clock-git
pkgver=r1.01766e0
pkgrel=1
pkgdesc="A quick and dirty clock widget for WMII."
arch=('i686' 'x86_64')
url="https://github.com/bwhmather/wmii-clock"
license=('MIT')
categories=()
depends=('wmii')
makedepends=('git')
provides=(wmii-clock)
conflicts=(wmii-clock)
source=("wmii-clock::git+$url")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/wmii-clock"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "$srcdir/wmii-clock"
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  cd "$srcdir/wmii-clock"
  make PREFIX=/usr DESTDIR="$pkgdir" install
}

