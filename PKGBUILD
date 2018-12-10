pkgname=('python3-pexpect')
pkgver=4.6.0
pkgrel=1
pkgdesc='For controlling and automating applications'
arch=('any')
url='https://pexpect.readthedocs.org/en/stable/'
license=('MIT')
makedepends=('git' 'python3' 'python3-ptyprocess')
source=("git+https://github.com/pexpect/pexpect#tag=${pkgver%%.0}")
sha512sums=('SKIP')

package_python3-pexpect() {
  cd pexpect
  python3 setup.py install --root="$pkgdir"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
