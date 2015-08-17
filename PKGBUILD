# Maintainer: archtux <antonio dot arias99999 at gmail.com>

pkgname=nomnom
pkgver=0.3.1
pkgrel=2
pkgdesc="Application for downloading videos from Youtube and other similar video websites"
arch=('i686' 'x86_64')
url="http://nomnom.sourceforge.net/"
license=('GPL3')
depends=('qjson' 'quvi' 'umph')
source=(http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz)
conflicts=('nomnom-git')
md5sums=('68ce70a51ad57ebc4ec872b52c2d4d41')


build() {
  cd $srcdir/$pkgname-$pkgver

  ./configure --prefix=/usr
  make
  make DESTDIR=$pkgdir install

  # Fix desktop file
  sed -i 's_nomnom.xpm_/usr/share/pixmaps/nomnom.xpm_' $pkgdir/usr/share/applications/nomnom.desktop
}
