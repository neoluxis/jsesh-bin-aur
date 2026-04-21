# Maintainer: Neolux Lee <aur.neolux@neolux.cn.eu.org>

pkgname=jsesh-bin
pkgver=7.11
pkgrel=1
pkgdesc="Hieroglyphic text editor packaged from the upstream JSesh binary release"
arch=('any')
url='https://github.com/rosmord/jsesh'
license=('custom:CeCILL' 'custom:jsesh-fonts')
depends=('jre21-openjdk')
makedepends=('unzip')
source=(
  "https://github.com/rosmord/jsesh/releases/download/release-${pkgver}/JSesh-${pkgver}.zip"
  'jsesh'
)
noextract=("JSesh-${pkgver}.zip")
sha256sums=(
  'SKIP'
  '618b985c21380ac91af6df947b34a056595f32f1539974d70c65a4b1a4aa1f66'
)

package() {
  cd "${srcdir}"

  unzip -oq "JSesh-${pkgver}.zip"

  install -dm755 "${pkgdir}/opt/jsesh/${pkgver}"
  cp -a "JSesh-${pkgver}/." "${pkgdir}/opt/jsesh/${pkgver}/"

  install -Dm755 "jsesh" "${pkgdir}/usr/bin/jsesh"
  install -Dm644 "JSesh-${pkgver}/LICENSE.txt" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
  install -Dm644 "JSesh-${pkgver}/FONT-LICENSE.md" "${pkgdir}/usr/share/licenses/${pkgname}/FONT-LICENSE.md"
}
