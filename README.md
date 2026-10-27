# Pakla Hub 4.13

Ekibin, anların ve araçların. Windows x64 masaüstü uygulaması.

[Windows için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar Ayarlar → Güncellemeler → Güncelleme ara ile 4.13.0 paketini yükleyebilir. Bildirimler açıksa yeni sürüm açılışta duyurulur; kurulum kullanıcı seçimiyle başlar.

## Aradığın yere daha kolay geç

Ctrl+K artık sohbetler, sunucular, kanallar, klipler, oyunlar, eklediğin uygulamalar ve araç/bölümler için ayrı tür filtresi sunar. @arkadaş ve #kanal sorguları korunur. En fazla 80 sonuç gösterilir; toplam eşleşme sayısı ayrıca görünür. Ctrl+L arama alanını seçer. Listeler yüklenen hesap verileri ve yerel kütüphanenle sınırlıdır; tüm bilgisayar dosyalarını taramaz.

![Türlere göre hızlı arama](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.13.0/Pakla-Hizli-Arama.png)

Özel mesaj aramasında Türkçe karakterler sadeleştirilerek, birden fazla sözcük birlikte eşleştirilir. Tümünden / Benden / Arkadaşımdan filtresi bulunur. Yalnızca açık sohbette yüklenen en fazla 1000 mesaj taranır ve ilk 60 eşleşme gösterilir; tüm sunucu geçmişi aranmaz. Arama mesaj göndermez. Dar sonuç satırları ve mesaj isim/saat alanları da düzenlendi.

![Sohbet araması](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.13.0/Pakla-Sohbet-Arama.png)

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

Son dosyaların Kaspersky taraması: 36 nesne, 0 tespit, 0 şüphe, 0 hata. Bu sonuç tüm ürünler ve gelecek sürümler için garanti değildir. Ayrıntılar sürümün SECURITY.md, QUALITY-REPORT.md ve release-verification.json dosyalarındadır.

Destek: supportpakla@gmail.com