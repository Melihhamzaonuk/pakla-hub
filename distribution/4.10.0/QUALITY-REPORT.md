# Pakla Hub 4.10 kontrol raporu

27 Ekim 2026. Windows x64 / .NET Framework 4.8.

## Yeni akışlar

Native 1366×900 pencere, sahte HTTP sunucusu ve geçici dosyalar kullanıldı:

- Türkçe karakter katlama, çok sözcüklü ve @/# kapsamlı arama; yerel arama penceresinden kanal açma ve sohbet taslağını koruma.
- URL ayrıştırma: desteklenmeyen protokol, kullanıcı bilgisi, kontrol/biçim karakterleri ve aşırı uzun adreslerin reddi; uluslararası alan adı ve noktalama işaretleri. Link/copy vektörleri gerçekten çizildi.
- Paylaşılanlar: yalnızca seçili konuşma, aynı URL'leri birleştirme, tam adres incelemesini iptal etme, GIF/boş arama, küçük pencere/DPI satırları ve taslağı bozmadan alıntı.
- Uzak GIF nesnesi gösterilmeden yüklenmedi; tarayıcı açılmadı. Testte yalnızca yerel GIF kaynağı gösterildi.
- Çoklu seçim, toplu favori/koleksiyon düzenleme, diğer hesabı dışlama, filtre değişiminde temizleme ve iki sayfada 31 klip seçimi.
- Yapay kayıt hatasında favori/koleksiyon değerlerinin geri alınması; geçersiz koleksiyon adı reddi. Video test dosyalarının baytları değişmedi.
- Başka ekrana ve hesaba geçince seçim modunun kapanması.

## Görünüm ve önceki davranışlar

12 ekran, beş istenen pencere boyutunda kontrol edildi. Minimum pencere sınırı geçerlidir. Native 144 DPI ve test ölçeğiyle 96/192 DPI kullanıldı; fiziksel monitör değiştirilmedi. Başlık sınırları/çakışma, dar bölüm menüsü, filtreler, profil sekmeleri, arama komutu ve kaydedilen sohbet genişliği geçti.

Önceki gelen kutusu, pin/hesap yalıtımı, geri/ileri, koleksiyon kaydı, özel görünüm kapatma, geç sosyal yanıt ve çevrimdışı yenileme senaryoları geçti. Keşif, taslak, alıntı, tepki/düzenleme/sabit, kanal yalıtımı, yeniden deneme nonce'ı ve DPAPI/oturum/çıkış yarışı testleri geçti. Dar kanal menüsünün yeni Paylaşılanlar komutunu içermesi dikkate alındı.

Uygulama özellik/yerel veri testleri, kurulum dosya özetleri/simge/kısayol/yeniden kurulum/veri koruma, RSA patch doğrulama, bozulmuş paket/yol taşması/eski sürüm reddi ve geri alma testleri geçti. 2.1, 4.3 ve 4.9 güncelleyicilerinden 4.10 kurulumu doğrulandı.

Son uygulama, kurulum, güncelleyici ve patch Kaspersky ile tarandı: 36 nesne, 0 tespit, 0 şüphe, 0 hata.

## Sınırlar

Gerçek kayıt, dış bağlantı açma, uzak GIF indirme, video dışa aktarma/silme, oyun açma veya gerçek kişilere mesaj gönderme yapılmadı. Görseller yerel test verileridir. Farklı ağlarda gerçek ses/ekran paylaşımı testi tamamlanmadı. Ses beta 6 kişi ve tek paylaşımla sınırlıdır; TURN/SFU yoktur. KLIPY üretim erişimi, Spotify OAuth ve güvenilir Windows yayıncı sertifikası henüz yoktur. Mesajlarda uçtan uca şifreleme bulunmaz. Bu rapor bütün hataların bittiği iddiası değildir.