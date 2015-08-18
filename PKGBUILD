# Contributer: CodeLinSoft

pkgname=youtubetomp3fix
name=YouTubeToMP3
pkgver=3.6
pkgrel=2
pkgdesc="A applications dedicated to playback, download and convert videos from YouTube"
arch=('i686' 'x86_64')
url="http://www.mediahuman.com/"
license=('GPL')
depends=('qt4' 'taglib' 'ffmpeg')
install="$pkgname.install"
#makedepends=('')

if [ "${CARCH}" = 'x86_64' ]; then
    ARCH='amd64'
    md5sums=('3d87f46e2b6cc06d998086375d754c01')
elif [ "${CARCH}" = 'i686' ]; then
    ARCH='i386' 
    md5sums=('936483cb7814476e3c966faf91e3ffbf')
fi
source=("http://www.mediahuman.com/download/${name}.$ARCH.deb")

build() {
  cd ${startdir}/src
  tar -zxf ${startdir}/src/data.tar.gz
}

package() {
  #sed -i '2s|Mp3|MP3|g' "$srcdir/usr/share/applications/youtube-to-mp3.desktop"
  sed -i '9s|Network|Application;Network|g' "$srcdir/usr/share/applications/youtube-to-mp3.desktop"
  sed -i '4s|Saves aoudio track from YouTube|Pulls audio tracks from YouTube videos|g' "$srcdir/usr/share/applications/youtube-to-mp3.desktop"
  cp -rp usr $pkgdir
  
}
