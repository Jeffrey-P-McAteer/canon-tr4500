# Maintainer: Jeffrey McAteer <jeffrey.p.mcateer@gmail.com>
pkgname=canon-tr4500
pkgver=current
pkgrel=2
pkgdesc="Package to install canon drivers and scan software from official RPM builds"
arch=('x86_64')
url="https://www.usa.canon.com/internet/portal/us/home/support/details/printers/inkjet-multifunction/tr-series-inkjet/pixma-tr4520/pixma-tr4520?tab=drivers_downloads"
license=('unknown')
depends=('libidn')
makedepends=('rpmextract')
options=('emptydirs')
source=(
  "http://gdlp01.c-wss.com/gds/9/0100009929/01/cnijfilter2-5.70-1-rpm.tar.gz"
  "http://gdlp01.c-wss.com/gds/2/0100009932/01/scangearmp2-3.70-1-rpm.tar.gz"
)
md5sums=(
  'bbac6322a820fcf8794f690226459a03'
  '34039812d38e093fb1c03ee4eb6ed14c'
)

package() {
  cd "$pkgdir"
  #tar xvf $(find . -name 'cnijfilter2-5.70-1-rpm.tar.gz' )
  rpmextract.sh $(find ../../.. -name 'cnijfilter2-5.70-1.x86_64.rpm' )
  #tar xvf $(find . -name 'scangearmp2-3.70-1-rpm.tar.gz' )
  rpmextract.sh $(find ../../.. -name 'scangearmp2-3.70-1.x86_64.rpm' )
  # This puts some libraries in ./usr/lib/ and some in ./usr/lib64
  # Arch symlinks /usr/lib64 to /usr/lib so we manually move stuff
  
  cp -r usr/lib64/* usr/lib/
  rm -rf usr/lib64

}

