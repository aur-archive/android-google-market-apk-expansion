# Maintainer: Jakub Schmidtke <sjakub-at-gmail-dot-com>

pkgname=android-google-market-apk-expansion
pkgver=r02
pkgrel=1
pkgdesc='Google Market APK Expansion library'
arch=('any')
url="http://developer.android.com/guide/market/expansion-files.html"
license=('custom')
depends=('android-sdk')
options=('!strip')
source=("https://dl-ssl.google.com/android/repository/market_apk_expansion-${pkgver}.zip" "source.properties")
md5sums=('fd5e8075df3e4b6e305823c53062b77b'
         'd9fd80f19d42a8b66d5c4e2fedaf71fd')

package() {
  mkdir -p "${pkgdir}/opt/android-sdk/extras/google/"
  mv "${srcdir}/google_market_apk_expansion" "${pkgdir}/opt/android-sdk/extras/google/play_apk_expansion"
  cp "${srcdir}/source.properties" "${pkgdir}/opt/android-sdk/extras/google/play_apk_expansion/"

  chmod -R ugo+rX "${pkgdir}/opt"
}
