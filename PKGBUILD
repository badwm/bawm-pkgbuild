pkgname="bawm"
pkgver=0.2
pkgrel=1
pkgdesc="A bad, but simple window manager for X"

arch=("x86_64")
license=('0BSD')

source=("https://github.com/badwm/bawm/archive/$pkgname-$pkgver.tar.gz")
build() {
  cd "bawm-$pkgname-${pkgver}"
  autoreconf || automake --add-missing
  ./configure
  make
}

package() {
  cd "$pkgname-${pkgver}"
  make DESTDIR="$pkgdir" install
}
md5sums=('e6149604e57ddcb95be99929270bde57')
