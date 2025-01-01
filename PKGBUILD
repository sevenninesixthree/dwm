pkgname=dwm
pkgver=$(git rev-parse --short HEAD)
pkgrel=1
pkgdesc="personal dwm version"
url="https://dwm.suckless.org"
arch=('x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft')
makedepends=('git')
provides=('dwm')
conflicts=('dwm')
source=(
   config.def.h
   config.h
   config.mk
   drw.c
   drw.h
   dwm.1
   dwm.c
   dwm.png
   LICENSE
   Makefile
   README
   transient.c
   util.c
   util.h
  )
sha256sums=(
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
  SKIP
)
build(){
  make
}
package(){
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}
