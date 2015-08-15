# Contributor: Jib <jbc dot as AT free dot fr>

pkgname=gnome-icons-breathe
_pkgname=breathe-icon-theme
pkgver=0.51
pkgrel=3
pkgdesc="A new effort to create a set of icons mixing the modern style of KDEs "Oxygen" icons with Ubuntu's "Human" set."
arch=('i686' 'x86_64')
depends=()
license=('CCPL:by-sa' 'GPL')
	# gnome-icons-breathe under CCPL; Arch icons under GPL
source=("http://launchpad.net/breathe-icon-set/trunk/${pkgver}/+download/${_pkgname}-${pkgver}.tar.gz" \
	"archlinux-128.png" \
	"archlinux-icon.svg")
url="https://launchpad.net/breathe-icon-set"
md5sums=('1654eeb36246adf2556b84595bfb6e07' \
	'23f29544a4eaed53f79cc2a4da5adc7f' \
	'eaaa839a58c2b62b71e30bfcf04a039a')

build() {
	install -d ${pkgdir}/usr/share/icons	
	mv ${srcdir}/${_pkgname}-${pkgver} ${pkgdir}/usr/share/icons
	
	#replace ubuntu logo with Arch logo
	convert -resize 16x16 ${startdir}/archlinux-128.png ${pkgdir}/usr/share/icons/${_pkgname}-${pkgver}/16x16/places/start-here.png
	convert -resize 22x22 ${startdir}/archlinux-128.png ${pkgdir}/usr/share/icons/${_pkgname}-${pkgver}/22x22/places/start-here.png
	convert -resize 24x24 ${startdir}/archlinux-128.png ${pkgdir}/usr/share/icons/${_pkgname}-${pkgver}/24x24/places/start-here.png
	convert -resize 32x32 ${startdir}/archlinux-128.png ${pkgdir}/usr/share/icons/${_pkgname}-${pkgver}/32x32/places/start-here.png
	install -D -m644 ${startdir}/archlinux-icon.svg ${pkgdir}/usr/share/icons/${_pkgname}-${pkgver}/scalable/places/start-here.svg
	}

