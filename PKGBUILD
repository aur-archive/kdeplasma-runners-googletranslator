# Maintainer: sxe <sxxe@gmx.de>

pkgname=kdeplasma-runners-googletranslator
pkgver=0.3.3
pkgrel=1
pkgdesc="A krunner plug-in that translates words using google. Forked version."
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/krunner-googletranslator?content=156498"
license=('GPL2')
depends=('kdebase-workspace' 'qjson')
makedepends=('cmake' 'automoc4')
conflicts=('google-translate-runner' 'kdeplasma-addons-runners-googletranslate' 'kdeplasma-runners-google-translate' 'kdeplasma-runners-googletranslate')
replaces=('google-translate-runner' 'kdeplasma-addons-runners-googletranslate' 'kdeplasma-runners-google-translate' 'kdeplasma-runners-googletranslate')
source=("http://kde-look.org/CONTENT/content-files/156498-translator.zip")

build() {

  rm -rf build

  mkdir build

  cd build

  cmake ../ \
    -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` \
    -DCMAKE_BUILD_TYPE=Release
  make
}

package() {
  cd build
  make DESTDIR="${pkgdir}" install
}
md5sums=('21fa173e94cc8dc3fa438c314770d0c4')
