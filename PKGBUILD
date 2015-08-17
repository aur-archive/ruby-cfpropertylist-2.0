# Maintainer: Brice Waegeneire <brice dot wge at gmail dot com>
# Contributor: Anshuman Bhaduri <anshuman (dot) bhaduri 0 (at) gmail
# (dot) com>

pkgname=ruby-cfpropertylist-2.0
_gemname=CFPropertyList
pkgver=2.0.17
pkgrel=1
pkgdesc="A module to read, write and manipulate property lists as defined by Apple."
arch=('any')
url="http://github.com/ckruse/CFPropertyList/"
license=('MIT')
depends=('ruby' 'libxml-ruby')
provides=('ruby-cfpropertylist')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
sha512sums=('5ed3f0b5906b379d224ddc811e542acc42ccf116520f957174985366b75d635df4f884fdf4440bc1db505d643f7e127120d86048886a82a26e87f7926640606e')
noextract=(${_gemname}-${pkgver}.gem)

package() {
  cd "${srcdir}"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies \
    -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}
