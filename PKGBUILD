# Maintainer: Neolux Lee <aur.neolux@neolux.cn.eu.org>

pkgname=jsesh-bin
pkgver=7.11
pkgrel=2
pkgdesc="Hieroglyphic text editor packaged from the upstream JSesh binary release"
arch=('any')
url='https://github.com/rosmord/jsesh'
license=('custom:CeCILL' 'custom:jsesh-fonts')
depends=('jre21-openjdk')
makedepends=('unzip')
source=(
  "https://github.com/rosmord/jsesh/releases/download/release-${pkgver}/JSesh-${pkgver}.zip"
  'jsesh'
  'jsesh.desktop'
  'jsesh-icon.png::https://jsesh.qenherkhopeshef.org/user/pages/01.home/logo.png'
)
noextract=("JSesh-${pkgver}.zip")
sha256sums=(
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
)

package() {
  cd "${srcdir}"

  unzip -oq "JSesh-${pkgver}.zip"

  install -dm755 "${pkgdir}/opt/jsesh/${pkgver}"
  cp -a "JSesh-${pkgver}/." "${pkgdir}/opt/jsesh/${pkgver}/"

  install -Dm755 "jsesh" "${pkgdir}/usr/bin/jsesh"
  install -Dm644 "JSesh-${pkgver}/LICENSE.txt" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
  install -Dm644 "JSesh-${pkgver}/FONT-LICENSE.md" "${pkgdir}/usr/share/licenses/${pkgname}/FONT-LICENSE.md"
  install -Dm644 "${srcdir}/jsesh.desktop" "${pkgdir}/usr/share/applications/jsesh.desktop"
  install -Dm644 "${srcdir}/jsesh.desktop" "${pkgdir}/usr/share/applications/jsesh.desktop"
  install -Dm644 "${srcdir}/jsesh-icon.png" "${pkgdir}/usr/share/icons/hicolor/48x48/apps/jsesh.png"
  install -Dm644 "${srcdir}/jsesh-icon.png" "${pkgdir}/usr/share/icons/hicolor/256x256/apps/jsesh.png"
}
