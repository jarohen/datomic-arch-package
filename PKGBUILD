pkgname=datomic-free
pkgver=0.1
pkgrel=1
pkgdesc="A package that installs Datomic (Free Edition) as a service"
arch=('any')
license=(EPL)
depends=('wget')
datomic-version=0.8.4159
source=(http://downloads.datomic.com/$datomic-version/datomic-free-$datomic-version.zip)
md5sums=('2c7a256d4d03405e5659e822687b646b')

build() { 
  cd "$srcdir/$pkgname-$pkgver/"
  ls
}

package() {
  cd "$srcdir/$pkgname-$pkgver/"
}
