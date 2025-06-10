pkgname=cargofetch
pkgver=0.1.4
pkgrel=1
pkgdesc="Cargofetch is a lightweight CLI tool written in Rust that fetches metadata about your Rust project."
arch=('x86_64')
url="https://github.com/arjav0703/cargofetch"
license=('MIT')
depends=( 'cargo')
makedepends=('cargo')
source=("$pkgname-$pkgver.tar.gz::https://github.com/arjav0703/cargofetch/archive/refs/tags/v$pkgver.tar.gz")
sha512sums=('SKIP')  # replace SKIP with real sha512sum or keep SKIP during testing

build() {
  cd "$srcdir/$pkgname-$pkgver"
  cargo build --release
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 "target/release/cargofetch" "$pkgdir/usr/bin/cargofetch"
}

