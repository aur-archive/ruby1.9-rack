# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Babken Vardanyan <483ken@gmail.com>

_gemname=rack
pkgname=ruby1.9-$_gemname
pkgver=1.4.5
pkgrel=1
pkgdesc='a modular Ruby webserver interface'
arch=(any)
url='http://rack.github.com/'
license=()
depends=(ruby1.9)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('2bfd9337cde2ad1dfdf14abfa8cee00b963e91cb')

package() {
  local _gemdir="$(ruby-1.9 -e'puts Gem.default_dir')"
  gem-1.9 install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/COPYING" "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
