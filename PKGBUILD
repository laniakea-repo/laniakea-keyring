# Maintainer: Aspen Schneider <rendezvous71@outlook.com>

pkgname=laniakea-keyring
pkgver=1
pkgrel=1
pkgdesc="Laniakea PGP keyring"
arch=('any')
url="https://github.com/laniakeaos/laniakea-keyring"
license=('MIT')
install=laniakea-keyring.install
depends=('pacman')
source=("https://github.com/laniakeaos/laniakea-keyring/releases/download/v${pkgver}/${pkgname}-${pkgver}.tar.gz"{,.sig})
sha256sums=('3d16690e98f264c9511bbfc40424a6e2cbafa92081c1e769ac92e5d5cb2ca652'
            'SKIP')
validpgpkeys=('425529067DE156F86814B55D2AE736768A7E87E6')

build() {
  cd laniakea-keyring-${pkgver}/

  make
}

package() {
  cd laniakea-keyring-${pkgver}/

  make DESTDIR=${pkgdir} PREFIX=/usr install
}
