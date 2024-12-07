license=("MIT")
arch=("any")
_pkgname=pexpect
pkgname=python3-${_pkgname}
pkgver=4.9
pkgrel=0
pkgdesc="For controlling and automating applications"
url="https://pexpect.readthedocs.org/en/stable/"
depends=("python3" "python3-ptyprocess")
makedepends=("python3-setuptools")
source=(
"https://github.com/pexpect/${_pkgname}/archive/refs/tags/${pkgver}.tar.gz"
"LICENSE::https://raw.githubusercontent.com/pexpect/${_pkgname}/master/LICENSE"
)
sha512sums=(
"222aa3a2aba174f1f9c9e5bbf71aa59fbc1c1830fce6691ecb01ec4f0613b1f2141da489a6bd7bfd226f46d98d52a16e1f5a5b7345bcf6557110bfd52cd5f31e"
"686daf49177ff5323500c8632007c4496d301e79e7caad751ebd635604429ba99dbc7db7399f42f631d891a80a8845d0dfdf579fd65436735a8fd12efdbcc8f8"
)

build() {
  cd ${_pkgname}-${pkgver}
  python3 setup.py build
}

package() {
  cd ${_pkgname}-${pkgver}
  python3 setup.py install --root="$pkgdir" --optimize=1 --skip-build
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
