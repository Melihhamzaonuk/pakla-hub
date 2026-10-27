# Pakla Hub 4.12

Ekibin, anların ve araçların. Windows x64 masaüstü uygulaması.

[Windows için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar Ayarlar → Güncellemeler → Güncelleme ara ile 4.12.0 paketini yükleyebilir. Bildirimler açıksa yeni sürüm açılışta duyurulur; kurulum kullanıcı seçimiyle başlar.

## Daha sade bir alan

Karşılama alanı küçültüldü, dekoratif hareketler kaldırıldı. Ana sayfadaki tekrar eden araç bölümü Araçlar sekmesinde kalır; boş taslak kartı gösterilmez. Nötr yüzeyler ve daha hafif kart başlıkları kullanılır. Üstteki kayıt simgesi yalnızca tampon açıkken görünür; kayıt başlatma ve ayarları Klipler bölümündedir. Oyun kartlarının düğmeleri küçük kartlarda da görünür kalır. Taslak listesi ürünün kendi renkleriyle yeniden çizilir.

![Sade ana sayfa](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.12.0/Pakla-AnaSayfa.png)

## Yazdığın yerden devam

Özel mesaj ve kanal taslakları bu bilgisayarda Windows hesabıyla şifrelenerek saklanır. Ctrl+Shift+D taslak listesini açar: önizle, sohbetine dön veya bir taslağı sil. Ana sayfa ve Ayarlar içinde de erişim bulunur. Taslaklar Pakla hesabına göre ayrılır; başka cihazlara eşitlenmez. Çıkış yapmak dosyayı silmez; taslak listesinden silebilirsin. Her türde en yeni 100 dolu taslak diskte saklanır. Okunamayan bir taslak dosyası otomatik olarak üzerine yazılmaz.

![Örnek taslaklar](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.12.0/Pakla-Taslaklar.png)

## Kısayollar elinin altında

F1 rehberi açar. Ctrl+K hızlı arama, Ctrl+Shift+D taslaklar, Alt+oklar ekran geçmişi, Ctrl+F seçili sohbet/kanalda arama. Tampon kaydını sen başlattıysan Ctrl+Shift+F8 son anları kaydeder.

Sohbet, topluluklar, GIF’ler, yerel klip kütüphanesi, koleksiyonlar, bilgisayar araçları ve önceki sürümün açılış/güncelleme düzeltmeleri korunur. Temizlik seçerek yapılır; bağlantı araçları ölçüm sağlar. FPS veya internet hızı artışı garanti edilmez.

## Geliştirme durumu

Ses/ekran paylaşımı beta: altı kişi, tek paylaşım; TURN/SFU yok. Gerçek farklı ağlarda mikrofon/ekran testleri tamamlanmadı. KLIPY ortak test kotası 100 API çağrısı/saat. Spotify OAuth yapılandırılmadı. Mesajlar uçtan uca şifreli değil. Windows yayıncı sertifikası bulunmuyor; patch paketleri ayrı RSA-SHA256 imzasıyla doğrulanır. Güvenlik korumalarını kapatma.

Son dosyaların Kaspersky taraması: 28 nesne, 0 tespit, 0 şüphe, 0 hata. Bu sonuç tüm ürünler ve gelecek sürümler için garanti değildir. Ayrıntılar sürümün SECURITY.md, QUALITY-REPORT.md ve release-verification.json dosyalarındadır.

Destek: supportpakla@gmail.com