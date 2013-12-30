pkgname=datomic-free
pkgver=0.1
pkgrel=2
pkgdesc="A package that installs Datomic (Free Edition) as a service"
packager="James Henderson"
arch=('any')
depends=('java-environment' 'maven')
url="http://www.datomic.com/"
license=('custom:DatomicFreeEditionLicense')

datomic_version=0.9.4384

source=(http://downloads.datomic.com/$datomic_version/datomic-free-${datomic_version}.zip transactor.properties datomic-free.service)
md5sums=('0183bbfc33951ff52166fedd6695f46f' '96a60a728a136b13854e628370f6d1d7' '70b657e22e7e2e8d4a558a662f96b7db')

package() {
  mkdir -p $pkgdir/usr/lib/ $pkgdir/usr/lib/systemd/system
  mkdir -p $pkgdir/var/lib/datomic/{data,log}
  cp -r "$srcdir/datomic-free-${datomic_version}" $pkgdir/usr/lib/datomic
  cp $srcdir/transactor.properties $pkgdir/usr/lib/datomic/config/
  cp $srcdir/datomic-free.service $pkgdir/usr/lib/systemd/system/
}

install=datomic.install