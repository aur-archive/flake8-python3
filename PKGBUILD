# Maintainer: spider-mario <spidermario@free.fr>
# Contributor: Allen Li <darkfeline at abagofapples.com>

pkgname=flake8-python3
pkgver=1.6.2
pkgrel=3
pkgdesc="Mixes pyflake and pep8 check, with an inline deactivation feature."
arch=('any')
url="http://bitbucket.org/tarek/flake8"
license=('custom:MIT')
depends=('python')
conflicts=('flake8')
options=(!emptydirs)
_pkgname=flake8
source=("http://pypi.python.org/packages/source/f/$_pkgname/$_pkgname-$pkgver.tar.gz")
md5sums=('abfdbb25d37c28e9da05f1b5c3596d1a')

build() {
    cd "$srcdir/$_pkgname-$pkgver"

    python setup.py install --root="$pkgdir/" --prefix=/usr --optimize=1
}

package() {
    cd "$srcdir/$_pkgname-$pkgver" 

    install --directory "$pkgdir/usr/share/licenses/$pkgname/"
    install --mode=644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/"
}

# vim:set ts=4 sw=4 et:
