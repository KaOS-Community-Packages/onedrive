pkgname=onedrive
pkgver=2.4.0
pkgrel=1
pkgdesc="Free OneDrive client written in D - abraunegg's fork. Follows the releases on https://github.com/abraunegg/onedrive/releases"
arch=('x86_64')
url="https://github.com/abraunegg/onedrive"
license=('GPL')
source=("https://github.com/abraunegg/onedrive/archive/v$pkgver.tar.gz")
depends=('curl' 'libnotify' 'sqlite' 'ldc')
makedepends=('dmd')

build() {
	cd "$pkgname-$pkgver"
        ./configure --sysconfdir=/etc --prefix=/usr --enable-notifications --enable-completions
        make
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR=$pkgdir PREFIX=/usr install
}
md5sums=('5f79426743be5828163ff4fc2e30e6e2')
