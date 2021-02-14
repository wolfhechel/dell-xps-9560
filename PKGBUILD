pkgname=dell-xps-9560
pkgver=0.r1.d944cb5
pkgrel=1
pkgdesc="Dell XPS 9560 tweaks"
arch=("any")
url="https://github.com/wolfhechel/dell-xps-9560"
license=("GPL3")
conflicts=("tpl")
source=("git+${url}.git")
sha256sums=("SKIP")

pkgver() {
    cd ${pkgname}
    printf "0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd ${pkgname}
    cp -r {etc,usr} ${pkgdir}
    chmod +x ${pkgdir}/usr/share/xps/udev-hooks/power-manager
}
