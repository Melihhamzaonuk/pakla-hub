# Pakla Hub 4.6

Sohbet, topluluklar, klipler ve bilgisayar araçları tek uygulamada.

[Windows x64 kurulumunu indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

## Bu güncellemede

- Discord benzeri kompakt sunucu şeridi, kanal kategorileri, sohbet ve üye düzeni.
- Özel mesajlarda yüklenen mesajlar içinde arama; sunucu kanallarında GIF/emoji paneli.
- Ekran değiştirmeden yenilenen okunmamış sunucu rozetleri.
- Kalıcı oturum, çevrimdışı yeniden bağlanma ve katıldığın özel sunucuları bulma düzeltmeleri.
- Pencere boyutuna uyarlanan bölmeler, sade mesaj çubuğu ve sunucudaki son kanalın hatırlanması.
- Ses kanalları ve ekran paylaşımı beta.

Pakla araçları sol şeritteki araç simgesinden açılır. Sunucu yönetimi için sunucu adına tıkla.

## Mevcut kullanıcılar

**Ayarlar → Güncellemeler → Güncelleme ara** yolunu açıp 4.6.0 paketini indir ve yükle. Yeniden kurulum gerekmez. Açılıştaki otomatik kontrol, güncelleme bildirimleri açıksa yeni sürümü bildirir; yükleme kullanıcı onayıyla yapılır. Çevrimdışı cihazlar sonraki başarılı kontrolde sürümü görür.

## Beta sınırları

Ses/ekran paylaşımı en fazla 6 kişi ve tek paylaşım içindir. TURN/SFU olmadığından bazı ağlarda bağlantı kurulamayabilir. Mikrofon ve ekran kaynağı kullanıcı izniyle açılır. Testler sentetik medya kullandı; farklı ağlarda gerçek mikrofon/ekran testi henüz tamamlanmadı.

Klipy ortak test kotası saatte 100 API isteğidir. GIF önce taslağa eklenir, Gönder ile paylaşılır. Alıcı uzak medyayı tıklayarak yükler. Özel mesajlarda uçtan uca şifreleme yoktur.

Spotify OAuth yapılandırılmadı; giriş sonrası tam oynatma doğrulanmadı. Internet Booster gecikme ölçer; VPN değildir. Oyun belleğine müdahale edilmez.

Windows 10/11 x64 ve .NET Framework 4.8 gerekir; ses ve Spotify görünümü Edge WebView2 kullanır. Patch RSA-SHA256 ile doğrulanır. Windows Authenticode yayıncı sertifikası henüz yoktur. Kaspersky taramasında tespit çıkmadı; bu tüm güvenlik ürünleri için garanti değildir.

Doğrulama: distribution/4.6.0 altındaki release-verification.json, SHA256SUMS.txt ve antivirus-report.txt. Lisanslar THIRD-PARTY-LICENSES.txt dosyasında ve uygulamadadır.

Destek: supportpakla@gmail.com