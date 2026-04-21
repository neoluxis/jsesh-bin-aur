pkgname=jsesh-bin
pkgver=7.11
pkgrel=1
pkgdesc="Hieroglyphic text editor packaged from the upstream JSesh binary release"
arch=('any')
url='https://github.com/rosmord/jsesh'
license=('custom:unknown')
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
}
