pkgname=('flask-session-cookie-manager3' 'flask-session-cookie-manager2')
_pkgname=flask-session-cookie-manager
pkgver=v1.2.1.1.r0.g3433273
pkgrel=1
pkgdesc='Decode and encode Flask session cookie'
arch=('any')
groups=('blackarch' 'blackarch-webapp')
url='https://noraj.github.io/flask-session-cookie-manager/'
license=('MIT')
makedepends=('git')
source=("git+https://github.com/noraj/$_pkgname.git")
sha512sums=('SKIP')

pkgver() {
  cd $_pkgname

  git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

package_flask-session-cookie-manager3() {
  cd $_pkgname
  depends+=('python' 'python-itsdangerous' 'python-flask')

  install -Dm 644 -t "$pkgdir/usr/share/doc/${_pkgname}3/" README.md
  install -Dm 644 LICENSE "$pkgdir/usr/share/licenses/${_pkgname}3/LICENSE"

  install -Dm 755 flask_session_cookie_manager3.py "$pkgdir/usr/bin/${_pkgname}3"
}

package_flask-session-cookie-manager2() {
  cd $_pkgname
  depends+=('python2' 'python2-itsdangerous' 'python2-flask')

  install -Dm 644 -t "$pkgdir/usr/share/doc/${_pkgname}2/" README.md
  install -Dm 644 LICENSE "$pkgdir/usr/share/licenses/${_pkgname}2/LICENSE"

  install -Dm 755 flask_session_cookie_manager2.py "$pkgdir/usr/bin/${_pkgname}2"
}
