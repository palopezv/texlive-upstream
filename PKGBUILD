# Maintainer: https://aur.archlinux.org/user/toropisco

INSTALL=0

if [[ $INSTALL == 0 ]]; then

  echo ""
  echo ""
  echo ""
  echo "This package REPLACES the texlive packages provided"
  echo ""
  echo "by Arch Linux with the UPSTREAM TexLive distribution."
  echo ""
  echo ""
  echo "This script will not do the homework for you;"
  echo ""
  echo "you are expected to install TeXLive on your own."
  echo ""
  echo ""
  echo "If you want to go ahead, you already know what to do."
  echo ""
  echo ""
  echo ""
  echo "Good luck."
  echo ""
  echo ""
  exit 1
else

  pkgname=texlive-upstream
  pkgver=3
  pkgrel=1
  pkgdesc="Install UPSTEAM by hand and REPLACE the distro packages COMPLETELY"
  url="http://www.tug.org/texlive/"
  arch=('any')
  license=('GPL')
  provides=('texlive-full' \
    'texlive-installer' \
    'texlive-most-doc' \
    'texlive-bin' \
    'texlive-htmlxml' \
    $(pacman -Sgq texlive-most texlive-lang)\
  )
  replaces=('texlive-full' \
    'texlive-installer' \
    'texlive-most-doc' \
    'texlive-bin' \
    'texlive-htmlxml' \
    $(pacman -Sgq texlive-most texlive-lang)\
  )
  conflicts=('texlive-full' \
    'texlive-installer' \
    'texlive-most-doc' \
    'texlive-bin' \
    'texlive-htmlxml' \
    $(pacman -Sgq texlive-most texlive-lang)\
  )
  options=('!strip')

  package() {
    mkdir -p "$pkgdir"/usr/share/doc/texlive-upstream

    echo "WARNING, NO WARRANTEE." >> "$pkgdir"/usr/share/doc/texlive-upstream/README
    echo "" >> "$pkgdir"/usr/share/doc/texlive-upstream/README
    echo "If you install TeXLive by hand, this package provides fake" > "$pkgdir"/usr/share/doc/texlive-upstream/README
    echo "distribution packages and some conflicting packages in AUR." >> "$pkgdir"/usr/share/doc/texlive-upstream/README
    echo "" >> "$pkgdir"/usr/share/doc/texlive-upstream/README
    echo "" >> "$pkgdir"/usr/share/doc/texlive-upstream/README
    echo "The author." >> "$pkgdir"/usr/share/doc/texlive-upstream/README
  }

fi
# vim:set ft=sh ts=2 sw=2 et:

