# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=colord-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="colord service for s6"
arch=(x86_64)
license=('beerware')
depends=('colord' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('colord.daemon.run'
		'colord.log.run'
		'colord.logd'
		'LICENSE')
md5sums=('62d62918e5a28bd7dd8ac7d243de4c2e'
         'ecd8eabb282d93790715093cf9fd0dd7'
         '722b6208ee337bf696026b30a5c82f68'
         '191a37ae657aa17e37e75d0242865dba')
validpgpkeys=('6DD4217456569BA711566AC7F06E8FDE7B45DAAC') # Eric Vidal

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/colord.daemon.run" "$pkgdir/etc/s6-serv/available/classic/colord/run"
	
	# log
	install -Dm 0755 "$srcdir/colord.log.run" "$pkgdir/etc/s6-serv/available/classic/colord/log/run"
	install -Dm 0644 "$srcdir/colord.logd" "$pkgdir/etc/s6-serv/log.d/serv/colord"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/colord-s6serv/LICENSE"
}
