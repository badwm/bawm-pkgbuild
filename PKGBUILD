pkgname="bawm"
pkgver=0.1
pkgrel=1
pkgdesc="A bad, but simple window manager for X"

arch=("x86_64")
license=('0BSD')

source=("https://github.com/badwm/bawm/archive/$pkgname-$pkgver.tar.gz")
build() {
  cd "$pkgname-${pkgver}"
  ./configure
  make
}

package() {
  cd "$pkgname-${pkgver}"
  make DESTDIR="$pkgdir" install
}
