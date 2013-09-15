pkgname=datomic-free
pkgver=0.1
pkgrel=1
pkgdesc="A package that installs Datomic (Free Edition) as a service"
packager="James Henderson"
arch=('any')
depends=('java-environment' 'maven')
url="http://www.datomic.com/"
license=('custom:DatomicFreeEditionLicense')

datomic_version=0.8.4159

source=(http://downloads.datomic.com/$datomic_version/datomic-free-${datomic_version}.zip transactor.properties datomic-free.service)
md5sums=('2c7a256d4d03405e5659e822687b646b' '96a60a728a136b13854e628370f6d1d7' 'e81463dbcdd55695bd76ba968d839a4f')

package() {
  mkdir -p $pkgdir/usr/lib/ $pkgdir/usr/lib/systemd/system
  mkdir -p $pkgdir/var/lib/datomic/{data,log}
  cp -r "$srcdir/datomic-free-${datomic_version}" $pkgdir/usr/lib/datomic
  cp $srcdir/transactor.properties $pkgdir/usr/lib/datomic/config/
  cp $srcdir/datomic-free.service $pkgdir/usr/lib/systemd/system/
}

install=datomic.install