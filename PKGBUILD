pkgname=gimp-plugin-vtf
pkgver=1.1+5+g5262e64
pkgrel=1
pkgdesc="Valve VTF file format plug-in for GIMP on Linux"
url="https://github.com/linux-source-tools/gimp-plugin-vtf"
arch=(x86_64)
license=(unknown)
depends=(gimp)
makedepends=(cmake boost)
# Not sure if we should use latest--so let's just stick to a safe commit
_commit=5262e641eb418fb20fcb20a2be48e8311b258222
source=("git+https://github.com/linux-source-tools/gimp-plugin-vtf.git#commit=$_commit")
sha256sums=('SKIP')

pkgver() {
  cd "$pkgname"
  git describe --tags | sed 's/-/+/g'
}

build() {
  cd "$pkgname"
  make
}

package() {
  cd "$pkgname"
  mkdir -p "${pkgdir}/usr/lib/gimp/2.0/plug-ins/"
  cp file-vtf "${pkgdir}/usr/lib/gimp/2.0/plug-ins/file-vtf"
}
