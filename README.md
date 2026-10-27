# Pakla Hub 4.9

Sohbet, topluluklar, klipler ve bilgisayar araçları aynı uygulamada.

[Windows x64 için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar **Ayarlar → Güncellemeler → Güncelleme ara** ile 4.9.0 paketini yükleyebilir. Kütüphane ve hesap verileri korunur. Bildirimler açıksa açılışta ve uygulama açıkken altı saatte bir sürüm kontrol edilir. Kurulum kullanıcı onayıyla yapılır.

## 4.9 yenilikleri

- **Gelen kutusu:** üst çubuktaki kutu simgesinden okunmamış özel mesajlara, arkadaşlık isteklerine ve kanallara ulaş. Rozetler bekleyen öğeleri gösterir. Veriler uygulama açıkken periyodik olarak yenilenir.
- **Sabit sohbetler:** sohbet listesinde sağ tıkla veya sohbet seçeneklerinden sabitle. En fazla 30 sabit sohbet bu cihazda, hesaba özel saklanır.
- **Okunmamış filtresi:** sohbet listesindeki Tümü/Yeni düğmeleriyle filtrele; yazdığın taslak ve açık sohbet korunur.
- **Geri/ileri:** yerel uygulama ekranlarında Alt+Sol ve Alt+Sağ. Açık sohbet ve sunucu bağlamı hatırlanır; geçmiş hesap değişiminde temizlenir. Ctrl+K aramasından da bu komutları bulabilirsin.
- **Klip koleksiyonları:** klibin üç nokta menüsündeki düzenleme ekranında koleksiyon adı yaz. Kütüphanedeki koleksiyon filtresiyle bul. Boş ad koleksiyonu kaldırır. Video dosyaları taşınmaz veya yeniden kodlanmaz.
- **Hesap korumaları:** eski hesabın özel ekranları ve uygulama içi diyalogları kapanır; geç gelen sosyal yanıtlar uygulanmaz. Kayıt tamponu, kaydı başlatan hesaba bağlı kalır. Kayıt sürerken çıkış düğmesi önce kaydetmeni ve durdurmanı ister.

4.8'in sabit gezinmesi, klip önizlemeleri, profil sekmeleri ve ayarlanabilir sohbet genişliği korunur. Klipler kendiliğinden paylaşılmaz veya yüklenmez.

![Gelen kutusu — test kişileri ve mesaj sayıları](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.9.0/Pakla-GelenKutusu.png)

![Klip koleksiyonları — test kapakları](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.9.0/Pakla-Koleksiyonlar.png)

Bu görsellerdeki kişiler, kapaklar ve klipler yerel test verileridir; uygulamayla kullanıcıya eklenmez.

## Mevcut sınırlar

Ses/ekran beta: 6 kişi, tek paylaşım; TURN/SFU yok, bazı ağlar bağlanamayabilir. Farklı ağlarda gerçek mikrofon ve ekran seçimi testi tamamlanmadı. KLIPY ortak test kotası saatte 100 API isteğidir. Spotify OAuth yapılandırılmadı; giriş sonrası tam oynatma doğrulanmadı. Mesajlarda uçtan uca şifreleme yoktur. Internet Booster bağlantı ölçümü yapar; VPN değildir. Oyun belleğine ve anti-cheat sistemlerine müdahale edilmez.

Windows 10/11 x64, .NET Framework 4.8 ve ses/Spotify için Edge WebView2 Runtime gerekir. Patch RSA-SHA256 ile doğrulanır. Windows Authenticode yayıncı sertifikası henüz yoktur. Son dosyaların Kaspersky taramasında 28 nesne, 0 tespit, 0 şüphe ve 0 hata görüldü; tüm güvenlik ürünleri için garanti değildir.

Kontroller: QUALITY-REPORT.md, release-verification.json, SHA256SUMS.txt, antivirus-report.txt ve SECURITY.md. Üçüncü taraf lisansları uygulamada ve THIRD-PARTY-LICENSES.txt dosyasındadır.

Destek: supportpakla@gmail.com