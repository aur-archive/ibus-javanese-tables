# Maintainer: Andry Widya Putra <andrywidyaputra@gmail.com>
pkgname=ibus-javanese-tables
pkgver=1
pkgrel=2
pkgdesc="A Javanese Script input method table for ibus"
arch=('any')
url="http://www.computer-issue.blogspot.com"
license=('GPL')
depends=('ibus' 'ibus-table')
optdepends=('ttf-tuladha-jejeg')
install=$pkgname.install
source=($pkgname-$pkgver.tar.gz)
md5sums=('28e44757780ece8c6e4e6c8ad685ab51') #generate with 'makepkg -g'

package() {
	mkdir -p $pkgdir/usr/share/ibus-table/tables/
	mkdir -p $pkgdir/usr/share/ibus-table/icons/
	ibus-table-createdb -n "$pkgdir/usr/share/ibus-table/tables/Javanese.db" -s "$srcdir/$pkgname-$pkgver/Javanese.txt"
	cp "$srcdir/$pkgname-$pkgver/Javanese.svg" "$pkgdir/usr/share/ibus-table/icons/Javanese.svg"
}
