# AnimeciX Linux

[animecix.net](https://animecix.net) web sitesinin Linux uygulamasıdır.

[Electron](https://www.electronjs.org/)  ile oluşturulmuştur. Typescript ile yazılmıştır.

## Özellikler
- Kaldığın yerden devam et
- Reklamsız video oynatma
- Otomatik sonraki bölüme geçme
- Videoları indirme
- Multi-Thread indirme

## Kurulum

Eğer Arch tabanlı bir dağıtım kullanıyorsanız AUR üzerinden kurabilirsiniz:

```sh
yay -S animecix-desktop-bin
```

Eğer başka bir dağıtım kullanıyorsanız:

[Buradan](https://github.com/RamazanMuslu/animecix-linux/releases) AppImage dosyası ile kullanabilirsiniz.

> **İpucu:** AppImage'ı sisteminize entegre etmek (menüye eklemek) için [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher) kullanmanızı öneririz.

## Geliştirme

Cihazınızda NodeJS kurulduğundan emin olun.

```sh
git clone https://github.com/RamazanMuslu/animecix-linux.git
```
İndirdikten veya klonladıktan sonra klasör içerisinde:

```sh
npm install
```
komutunu çalıştırın.

### Yararlı Komutlar

```sh
npm run compile #Typescript derlemesi yapar ve gerekli JavaScript dosyalarını oluşturur.
```

```sh
npm start #Compile kodu ile birlikte Electron uygulamasını başlatır
```

```sh
npm run build # Linux için .AppImage dosyasını oluşturur.
```

## İletişim

Orijinal Repo'nun geliştiricisiyle iletişime geçmek için:

- [discord.gg/animecix](https://discord.com/invite/animecix) 
- Discord: [CaptainSP#9999](https://discord.com/users/344220078465744896)
- Mail: [onmuapps@gmail.com](mailto://onmuapps@gmail.com) 
- Orijinal Repo: [https://github.com/CaptainSP/animecix-desktop](https://github.com/CaptainSP/animecix-desktop)

## License

GPL
