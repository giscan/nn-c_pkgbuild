# Maintainer: Sylvain POULAIN <sylvain.poulain@giscan.com>

pkgname=nnbathy
pkgver=1.86
pkgrel=1
pkgdesc="Provides Natural Neighbours interpolation library "libnn.a" and a command line Natural Neighbours interpolation utility nnbathy"
arch=('i686' 'x86_64')
makedepends=('triangle')
url="https://github.com/sakov/nn-c"
license=('GPLv3')
source=($pkgname-$pkgver.zip::"https://github.com/sakov/nn-c/archive/master.zip")
md5sums=('ecdde06128be6731deec081ebdeb7b3b')

build() {
	cd $srcdir/nn-c-master/nn/
	./configure --prefix=/usr
	make

}

package() {
  install -Dm644 $srcdir/nn-c-master/nn/libnn.a $pkgdir/usr/lib/libnn.a
  install -Dm644 $srcdir/nn-c-master/nn/nn.h $pkgdir/usr/include/nn.h
  install -Dm755 $srcdir/nn-c-master/nn/$pkgname /$pkgdir/usr/bin/$pkgname
}
