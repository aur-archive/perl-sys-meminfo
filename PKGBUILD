# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.23

pkgname='perl-sys-meminfo'
pkgver='0.91'
pkgrel='1'
pkgdesc=""
arch=('i686' 'x86_64')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl')
makedepends=()
url='http://search.cpan.org/dist/Sys-MemInfo'
source=('http://search.cpan.org/CPAN/authors/id/S/SC/SCRESTO/Sys-MemInfo-0.91.tar.gz')
md5sums=('d2ddda32c58114352e04ecb866de7f17')
sha512sums=('f34f6383b28f15dbfee80ff96b7b0a6102d3f187443b4697d4e1e58bc2ca1fdd7e4352907539648df0aaa1041d5278a7f31d03adfe5349889f426b5a941d5877')
_distdir="${srcdir}/Sys-MemInfo"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
