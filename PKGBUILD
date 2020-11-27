# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <crono1023@gmail.com>
pkgname="nano"
pkgver=5.3
pkgrel=1
epoch=
pkgdesc="gnu nano text editor"
arch=(x86_64)
url=""
license=('GPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://git.savannah.gnu.org/cgit/nano.git/snapshot/nano-5.3.tar.gz")
noextract=()
md5sums=()
validpgpkeys=()

build() {
	cd "$pkgname-$pkgver"
	./autogen.sh	
	./configure --prefix=/usr
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir" install
}
md5sums=('c6c1c42d85639197b3b0a454d48e0b93')
