# Maintainer: Caleb Bredekamp
pkgname=csb-bspwm-conf-git
_pkgname=csb-bspwm-conf
pkgver=v0.0.1.r3.g9260d84
pkgrel=1
_destname1="/etc/skel/.config/bspwm/"
pkgdesc="Caleb's bspwm configuration"
arch=('any')
url="https://github.com/caleb-sb/${_pkgname}.git"
license=('MIT')
depends=('bspwm')
makedepends=('git')
replaces=('arcolinux-bspwm-git')
provides=("${pkgname}")
conflicts=()
options=(!strip !emptydirs)
source=(${_pkgname}::"git+${url}")
sha256sums=('SKIP')
package() {
	install -dm 755 ${pkgdir}${_destname1}
	cp -r ${srcdir}/${_pkgname}/* ${pkgdir}${_destname1}
}
pkgver() {
	cd "$_pkgname"
	git describe --long | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}
