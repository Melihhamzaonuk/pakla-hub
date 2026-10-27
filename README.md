# Pakla Hub 4.7

Sohbet, topluluklar, klipler ve bilgisayar araçları tek uygulamada.

[Windows x64 kurulumunu indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar **Ayarlar → Güncellemeler → Güncelleme ara** yolundan 4.7.0 paketini yükleyebilir. Kullanıcı verileri korunur. Bildirimler açıksa açılışta ve uygulama açıkken altı saatte bir yeni sürüm kontrol edilir; kurulum kullanıcı onayıyla yapılır.

## 4.7 yenilikleri

- Özel mesajlarda yukarıda okurken gelen mesajlar ekranı aşağı çekmez. **Yeni mesajlar** ile en sona dönülür.
- Okundu durumu yalnızca odaktaki sohbetin sonu görüntülenirken gönderilir. Hesap değişiminden kalan yanıtlar uygulanmaz.
- Keşfette yeni arama yüklenirken eski sonuçlar temizlenir. Başarısız aramada yeniden deneme sunulur; geç dönen eski arama yeni sonuçları ezmez.
- Sunucu değiştirirken önceki kanalın eski mesaj konumu taşınmaz.
- Dar pencerede geçmiş ve sabitlenmiş mesajlar **Diğer kanal işlemleri** menüsünden açılır.
- Dolu veya salt okunur mesaj kutularına alıntı/emoji eklenmesi güvenli biçimde engellenir. Pano kullanım hatası uygulamayı kapatmaz.
- Uzun özel sohbetlerin bellekteki 1.000 mesaj sınırı açıklanır. Gönderim sırasında ekran değişse bile düğme durumu doğru yenilenir.
- Ses görünümü açılamazsa uygulamayı kapatmadan yeniden başlatılabilir.
- Mikrofon/ekran izni beklenirken kanaldan ayrılınca geç gelen medya durdurulur. Çift tıklama yeni izin pencereleri açmaz. İptal edilen ses katılımı sunucuda da temizlenir.

4.6'daki kompakt sunucu/kanal düzeni, GIF/emoji, sohbet araması, kalıcı oturum ve Pakla araçları korunur.

## Mevcut sınırlar

Ses/ekran paylaşımı beta: en fazla 6 kişi, aynı anda tek ekran. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. İki gerçek WebView2 bağlantısı sentetik ses/video ile test edildi; farklı ağlarda gerçek mikrofon ve ekran seçimi henüz uçtan uca doğrulanmadı. Gizli test pencerelerinin başlatılması bazı denemelerde zaman aşımına uğradı; kontrol tanıtıcıları oluşturulan yeniden başlatma testi ve iki görünüm testi geçti.

KLIPY ortak test kotası saatte 100 API isteğidir. GIF önce taslağa eklenir ve Gönder ile paylaşılır; alıcı uzak medyayı tıklayarak yükler. Özel mesajlarda uçtan uca şifreleme yoktur. Spotify OAuth yapılandırılmadı, giriş sonrası tam oynatma doğrulanmadı.

Internet Booster bağlantı ölçümü yapar; VPN değildir. Oyun belleğine müdahale edilmez. Windows 10/11 x64 ve .NET Framework 4.8 gerekir; ses/Spotify için Edge WebView2 Runtime kullanılır.

Patch RSA-SHA256 ile doğrulanır; Windows Authenticode yayıncı sertifikası henüz yoktur. Son dosyaların Kaspersky taramasında 28 nesne, 0 tespit, 0 şüphe ve 0 hata görüldü. Bu, tüm güvenlik ürünleri için garanti değildir.

Doğrulama dosyaları: distribution/4.7.0/release-verification.json, SHA256SUMS.txt, antivirus-report.txt ve SECURITY.md. Üçüncü taraf lisansları THIRD-PARTY-LICENSES.txt ve uygulamada bulunur.

Destek: supportpakla@gmail.com