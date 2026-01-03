# Maintainer: Ramazan Muslu <ramazanmuslu@yorastudioplus.com>
pkgname=animecix-desktop-bin
pkgver=1.3.1
pkgrel=1
pkgdesc="AnimeciX Desktop App"
arch=('x86_64')
url="https://github.com/RamazanMuslu/animecix-linux"
license=('GPL')
depends=('gtk3' 'nss' 'alsa-lib')
provides=('animecix-desktop')
conflicts=('animecix-desktop')
# Varsayılan olarak GitHub Release'den AppImage çeker.
# Yayına almadan önce release oluşturmalı ve checksum'ı güncellemelisiniz.
_filename="animecix-${pkgver}.AppImage"
source=("https://github.com/RamazanMuslu/animecix-linux/releases/download/v${pkgver}/${_filename}")
sha256sums=('SKIP') # 'sha256sum dosyaadi' komutuyla alıp buraya yazın

prepare() {
    chmod +x "${_filename}"
    ./"${_filename}" --appimage-extract
}

package() {
    # AppImage içeriğini sistem dizinlerine kopyalama
    # Not: AppImage yapısı Electron Builder'a göre değişebilir, standart yapı varsayılmıştır.
    
    install -d "${pkgdir}/opt/animecix-desktop"
    cp -r "${srcdir}/squashfs-root/"* "${pkgdir}/opt/animecix-desktop/"
    
    # Binary sembolik linki
    install -d "${pkgdir}/usr/bin"
    ln -s "/opt/animecix-desktop/AppRun" "${pkgdir}/usr/bin/animecix-desktop"
    
    # Desktop dosyası (.desktop dosyasının AppImage içinde olduğunu varsayıyoruz)
    install -Dm644 "${srcdir}/squashfs-root/animecix.desktop" "${pkgdir}/usr/share/applications/animecix-desktop.desktop"
    
    # İkon (varsa)
    if [ -f "${srcdir}/squashfs-root/animecix.png" ]; then
        install -Dm644 "${srcdir}/squashfs-root/animecix.png" "${pkgdir}/usr/share/icons/hicolor/512x512/apps/animecix-desktop.png"
    fi
}
