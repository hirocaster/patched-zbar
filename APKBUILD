pkgname=zbar
pkgver=0.10
pkgrel=1
pkgdesc="Port of ZBAR BAR CODE READER"
url="http://zbar.sourceforge.net/"
arch="all !aarch64"
license="LGPL2+"
depends="py-gobject"
makedepends="imagemagick-dev gtk+-dev py-gtk-dev qt-dev libtool lcms2-dev"
install=""
subpackages="$pkgname-dev $pkgname-doc"
source="https://github.com/hirocaster/patched-zbar/raw/master/zbar-0.10.tar.bz2"

builddir="$srcdir"/zbar-$pkgver
build() {
	cd "$builddir"
	./configure --prefix=/usr --disable-video || return 1
	make || return 1
}

package() {
	cd "$builddir"
	ls
	make DESTDIR="$pkgdir" install
}

md5sums="70ac2549bed2c22e09c759ee72c43ebd  zbar-0.10.tar.bz2"
sha256sums="501c17bfc5a93a54777e35a6cb795abc5654029ebc3f5343e6b0f99f72484c57  zbar-0.10.tar.bz2"
sha512sums="6806fb5d5886e1c51ab1a4dd01d362d41326b789d23f89905af71f188307e502f39a2b8fb853fe9ccb4b6dff4cc11f8fe13e81665567c5841b63a5f77ee364f8  zbar-0.10.tar.bz2"
