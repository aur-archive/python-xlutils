# Maintainer: Aaron DeVore <aaron.devore@gmail.com>
# Contributor: jan.scevlik <jan.scevlik@gmail.com>
# Contributor: tocer <tocer.deng@gmail.com>

pkgname=python-xlutils
pkgver=1.7.1
pkgrel=1
pkgdesc="Utilities for working with Excel files"
arch=(any)
url="http://www.simplistix.co.uk/software/python/xlutils"
license=(MIT)
depends=('python2' 'python2-xlrd' 'python2-xlwt')
optdepends=('python2-errorhandler: ErrorFilter support')
makedepends=(python2-setuptools)
provides=(python2-xlutils)
conflicts=(python2-xlutils)
source=("http://pypi.python.org/packages/source/x/xlutils/xlutils-$pkgver.tar.gz")
md5sums=('6247ccda7d8f864b815525e94da30977')

build() {
  cd "$srcdir/xlutils-$pkgver"
  python2 setup.py build
}

package() {
  cd "$srcdir/xlutils-$pkgver"
  python2 setup.py install --root="$pkgdir/" --optimize=1
  install -Dm644 xlutils/license.txt \
    "$pkgdir/usr/share/licenses/$pkgname/license.txt"
}
 
# xlutils has a test suite, but it requires 5 extra package just for
# checking. Too much for an AUR package.

