# Maintainer: hamki <hamki.do2000@gmail.com>
pkgname=syncstorage-rs
pkgver=0.8.5
pkgrel=1
epoch=
pkgdesc="Mozilla Sync Storage built with Rust."
arch=('i686' 'x86_64')
url="https://github.com/mozilla-services/syncstorage-rs"
license=('MPL2')
groups=()
depends=('rust')
makedepends=('make gcc rust go')
checkdepends=()
optdepends=('mariadb')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/mozilla-services/$pkgname/archive/$pkgver.tar.gz")
noextract=()
sha256sums=(8a08b2e836eec0f8f922f560c65092f57feb141d5cd551413029a9e690939399)

prepare() {
  cd "$srcdir/$pkgname-$pkgver"

}

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
}
