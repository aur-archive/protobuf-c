# Maintainer: Aurélien Wailly <aurelien.wailly@gmail.com>

pkgname=protobuf-c
pkgver=0.15
pkgrel=3
pkgdesc="C bindings for Google's Protocol Buffers"
arch=('i686' 'x86_64')
url="http://code.google.com/p/protobuf-c/"
license=('Apache')
depends=('protobuf')
options=(!libtool)
source=(http://$pkgname.googlecode.com/files/$pkgname-$pkgver.tar.gz)
md5sums=('73ff0c8df50d2eee75269ad8f8c07dc8')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	./configure --prefix=/usr --disable-static
        # if you have compiling problems, uncomment the following line
	# export MAKEFLAGS=-j1
        make check
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir" install
}
