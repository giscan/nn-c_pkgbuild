# Maintainer: Sylvain POULAIN <sylvain.poulain@giscan.com>

pkgname=nnbathy
pkgver=1.86
pkgrel=1
pkgdesc="Provides Natural Neighbours interpolation library "libnn.a" and a command line Natural Neighbours interpolation utility nnbathy"
arch=('i686' 'x86_64')
makedepends=('triangle')
url="https://github.com/sakov/nn-c"
license=('GPLv3')
#source=("https://github.com/sakov/nn-c/archive/master.zip")
#md5sums=('')

build() {
	cd "$srcdir/"
	
	git clone https://github.com/sakov/nn-c/
	
	cd "$srcdir/nn-c/nn"
	./configure --prefix=/usr
	make

}

package() {
  cd "$srcdir/nn-c/nn"
  make DESTDIR="${pkgdir}" install
}
