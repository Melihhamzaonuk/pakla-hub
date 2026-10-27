# Pakla Hub 4.8

Sohbet, topluluklar, klipler ve bilgisayar araçları aynı çalışma alanında.

[Windows x64 için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar **Ayarlar → Güncellemeler → Güncelleme ara** ile 4.8.0 paketini yükleyebilir. Kütüphane ve hesap verileri korunur. Bildirimler açıksa açılışta ve uygulama açıkken altı saatte bir yeni sürüm kontrol edilir; yükleme kullanıcı onayıyla yapılır.

## Yeni çalışma alanı

- Her ekranda aynı ana gezinme: Ana sayfa, Sohbet, Klipler, Kitaplık ve Araçlar. Dar pencerelerde bölüm menüsü açılır.
- Ana sayfada kendi son oyunların, yerel kliplerin ve sohbet/topluluk kısayolların.
- Kliplerde içerik odaklı kütüphane; süre etiketleri, arama, sıralama ve favoriler. Kayıt ayarları ayrı ekranda, kayıt durumu küçük bir çubukta.
- Profilde genel bakış, klipler ve hesap sekmeleri; düzenlerken canlı metin önizlemesi.
- Sohbet/kanal listelerinin kenarını sürükleyerek genişliği ayarla. Tercih hatırlanır; kenara çift tıklayarak varsayılana dön.
- Ctrl+K ile simgeli arama: bölüm, oyun, uygulama ve bu hesaba ait yerel klipler. ↑/↓ seçer, Enter açar, Esc kapatır.
- Sakin koyu yüzeyler, tutarlı vurgu, daha sık aralıklar; bakım ve ayarlar sade satırlarda.

![Ana sayfa — örnek oyunlar ve test verileri](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.8.0/Pakla-AnaSayfa.png)

![Klipler — test videosu kapakları; gerçek kayıtlar değildir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.8.0/Pakla-Klipler.png)

Önizlemeler yerel test verileridir. Örnek oyunlar, kişiler ve klipler uygulamaya eklenmez. Ürün incelemesi ve tasarım çıkarımları [DESIGN-REFERENCES.md](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.8.0/DESIGN-REFERENCES.md) dosyasındadır. Marka varlıkları veya üçüncü taraf kaynak kodları kopyalanmadı.

## Bilinen sınırlar

Ses/ekran beta: 6 kişi, tek ekran paylaşımı, TURN/SFU yok; bazı ağlar bağlanamayabilir. Farklı ağlarda gerçek mikrofon ve ekran seçimi testi tamamlanmadı. KLIPY ortak test kotası saatte 100 API isteğidir. Spotify OAuth yapılandırılmadı; giriş sonrası tam oynatma doğrulanmadı. Klipler kendiliğinden buluta yüklenmez. Mesajlarda uçtan uca şifreleme yoktur.

Internet Booster gecikme/jitter/kayıp ölçer; VPN değildir. Oyun belleğine ve anti-cheat sistemlerine müdahale edilmez.

Windows 10/11 x64, .NET Framework 4.8 ve ses/Spotify için Edge WebView2 Runtime gerekir. Patch RSA-SHA256 ile doğrulanır. Güvenilir Windows Authenticode yayıncı sertifikası henüz yoktur. Son dosyaların Kaspersky taramasında 36 nesne, 0 tespit, 0 şüphe ve 0 hata görüldü; tüm güvenlik ürünleri için garanti değildir.

Kontroller: release-verification.json, QUALITY-REPORT.md, SHA256SUMS.txt ve antivirus-report.txt. Lisanslar THIRD-PARTY-LICENSES.txt ve uygulamada bulunur.

Destek: supportpakla@gmail.com