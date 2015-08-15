# Maintainer: BlackEagle < ike DOT devolder AT gmail DOT com >
# Contributor: Bram Schoenmakers <me@bramschoenmakers.nl>
pkgname=closure-compiler
pkgver=20120710
pkgrel=1
pkgdesc="Performs checking, instrumentation and optimizations on Javascript code."
arch=('any')
url="http://code.google.com/closure"
license=('APACHE')
depends=(java-runtime)
source=("http://$pkgname.googlecode.com/files/compiler-$pkgver.tar.gz")

package() {
	cd $srcdir

	install -m755 -D compiler.jar "$pkgdir/usr/share/java/closure-compiler/closure-compiler.jar"
	mkdir $pkgdir/usr/bin
	echo '#!/bin/sh
	"$JAVA_HOME/bin/java" -jar /usr/share/java/closure-compiler/closure-compiler.jar $@' > "$pkgdir/usr/bin/closure"
	chmod +x "$pkgdir/usr/bin/closure"
}
sha256sums=('73318c100e65d22879decaa3a2558b4fe5b9ab73c5c124d9526ac0c2cff070e2')
