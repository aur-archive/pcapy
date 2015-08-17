# Contributor: Tom Wambold <tom5760@gmail.com>
pkgname=pcapy
pkgver=0.10.5
pkgrel=3
pkgdesc="Python module for the libpcap packet capture library."
arch=('i686' 'x86_64')
url="http://oss.coresecurity.com/projects/pcapy.html"
license=('APACHE')
depends=('libpcap' 'python2')
source=(http://oss.coresecurity.com/repo/$pkgname-$pkgver.tar.gz
        LICENSE)
md5sums=('1dcff6af494f3d6763f457aa86aa0853'
         'aad04e351e4ddd12cac6158470d8d886')

build() {
    cd $startdir/src/$pkgname-$pkgver
    python2 setup.py install --root=$startdir/pkg || return 1
    install -D $startdir/src/LICENSE $startdir/pkg/usr/share/licenses/pcapy/LICENSE
}
