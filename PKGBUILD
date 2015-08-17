# Maintainer: Michael Spencer <sonrisesoftware@gmail.com>

pkgname=qml-desktop
pkgver=0.0.5
pkgrel=1
pkgdesc="A C++ plugin for QML to access desktop features for Papyros"
arch=("i686" "x86_64")
url="https://github.com/papyros/qml-desktop"
license=("LGPL")
depends=("qt5-base-git" "qt5-declarative-git" "libpulse" "glib2")
makedepends=("git")
provides=("$pkgname")
source=("$pkgname::git+https://github.com/papyros/qml-desktop.git#tag=v$pkgver")
sha256sums=("SKIP")

prepare() {
	mkdir -p build
	cd build
	qmake "$srcdir/$pkgname"
	make
}

package() {
	cd build
	make INSTALL_ROOT="$pkgdir" install
}
