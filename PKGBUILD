_pkgname=dwm
pkgname=$_pkgname-git
pkgver=6.5
pkgrel=2
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
provides=($_pkgname)
depends=('libx11' 'libxinerama' 'libxft' 'freetype2' 'st' 'dmenu')
source=('config.h' 'config.mk' 'drw.c' 'drw.h' 'dwm.1'
	'dwm.c' 'dwm.c' 'LICENSE' 'Makefile' 
	'transient.c' 'util.c' 'util.h')
md5sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP'
	'SKIP' 'SKIP' 'SKIP' 'SKIP'
	'SKIP' 'SKIP' 'SKIP')

build() {
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11 FREETYPEINC=/usr/include/freetype2
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
