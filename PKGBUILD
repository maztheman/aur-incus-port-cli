# Maintainer: Your Name <youremail@domain.com>
pkgname="incus-port-cli"
pkgver="1.0.2"
pkgrel="1"
pkgdesc="Updates incus portforwards dynamically"
arch=("any")
url="https://github.com/maztheman/${pkgname}"
license=('MIT')
groups=()
depends=()
makedepends=("cmake" "ninja" "gcc" "git")
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("${pkgname}-v${pkgver}.tar.gz::${url}/archive/refs/tags/${pkgver}.tar.gz")
noextract=()
sha256sums=('3cae40029c1ed81b4a0342c2b18f121fb9e1d21de30ab01a4780a5158a2eea0b')

build() {
  cd "$pkgname-$pkgver"

  cmake -B build -S . -GNinja -DCMAKE_INSTALL_PREFIX=/usr
  cmake --build build
}

package() {
  cd "$pkgname-$pkgver"
  cmake --install build --prefix "$pkgdir/usr"
}
