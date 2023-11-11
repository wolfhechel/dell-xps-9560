pkgname=dell-xps-9560
pkgver=0.r15.5c1b542
pkgrel=1
pkgdesc="Dell XPS 9560 tweaks"
arch=("any")
url="https://github.com/wolfhechel/dell-xps-9560"
license=("GPL3")
install=dell-xps-9560.install
conflicts=("tpl")
source=("git+${url}.git")
sha256sums=("SKIP")

pkgver() {
    cd ${pkgname}
    printf "0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd ${pkgname}
    cp -r etc ${pkgdir}
}
