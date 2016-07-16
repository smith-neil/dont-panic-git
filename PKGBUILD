# Maintainer: Neil Smith <smith.neil.h@gmail.com>

_pkgname=dont-panic

pkgname=dont-panic-git
pkgver=0.0.1.r0.g57155a3
pkgrel=1
pkgdesc="Prints system info, as well as the words \"Don't Panic\" in large friendly letters, to your terminal."
arch=('any')
url="https://github.com/smith-neil/dont-panic"
license=('GPL')
groups=()
depends=('bash')
makedepends=('git')
provides=($_pkgname)
source=('git+https://github.com/smith-neil/dont-panic.git')
md5sums=('SKIP')

pkgver() {
    cd "$srcdir/$_pkgname"
    git describe --tags --long | sed -r -e 's,^[^0-9]*,,;s,([^-]*-g),r\1,;s,[-_],.,g'
}

package() {
    cd "$srcdir/$_pkgname"
    install -Dm755 "$_pkgname" "$pkgdir/usr/bin/$pkgname"
}
