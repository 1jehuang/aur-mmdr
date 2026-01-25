# Maintainer: Jeremy <jeremy@local>

pkgname=mmdr-bin
pkgver=0.1.1
pkgrel=1
pkgdesc="Fast Mermaid renderer in Rust (flowchart/class/state/sequence)"
arch=('x86_64')
url="https://github.com/1jehuang/mermaid-rs-renderer"
license=('MIT')
depends=('glibc')
source=(
  "mmdr-${pkgver}-x86_64-unknown-linux-gnu.tar.gz::https://github.com/1jehuang/mermaid-rs-renderer/releases/download/v${pkgver}/mmdr-x86_64-unknown-linux-gnu.tar.gz"
  "LICENSE::https://raw.githubusercontent.com/1jehuang/mermaid-rs-renderer/v${pkgver}/LICENSE"
)
sha256sums=(
  '00a3bcad49a4c4a423046787e4ca9465c2bb4bd88e6b18a73601cc5b0197c7a5'
  '57ed7943c34463678a150769d4a4f6c95d2a190fe2c1977f74bc883492c94b86'
)

package() {
  install -Dm755 mmdr "${pkgdir}/usr/bin/mmdr"
  install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
