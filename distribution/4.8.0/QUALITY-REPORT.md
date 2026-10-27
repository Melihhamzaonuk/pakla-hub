# Pakla Hub 4.8 kontrol raporu

27 Ekim 2026. Windows x64 / .NET Framework 4.8.

## Tasarım ve kullanım

11 ürün ekranı, istenen beş pencere boyutunda kontrol edildi: Ana Sayfa, Mesajlar, Topluluklar, Sunucu Keşfet, Klipler, Kayıt Ayarları, Kitaplık, Araçlar, Profil, Ayarlar ve Müzik. Uygulamanın minimum pencere sınırı geçerlidir. Native 144 DPI yanında 96/192 DPI için test ölçekleri kullanıldı; fiziksel monitör/DPI değiştirilmedi.

Başlık düğmelerinin sınırları ve birbirleriyle çakışmaması, dar pencere bölüm menüsü, klip araması/favoriler/boş filtre sonucu, profil sekmeleri, arama paletinde sonuç temizliği ve seçilen komutun açılması doğrulandı. Sohbet genişliğinin iki görünümde paylaşılması, dosyaya kaydedilmesi ve çift tıklamayla sıfırlanması test edildi. Aktif ses görünümünün bölüm değişiminde korunması, ses denetimlerinin yeniden görünmesi ve ayrılma durumu fixture kontrolüyle doğrulandı; gerçek mikrofon kullanılmadı.

Ana sayfa, sohbet, sunucu, klip, profil, kitaplık ve araç ekranlarının native render'ları incelendi. Görsellerdeki kişiler, kapaklar ve klipler test verisidir; kullanıcıya yüklenmez ve buluta gönderilmez. Kayıt veya oyun başlatılmadı.

## Korunan davranışlar

- Keşif: yükleme/boş/hata/yeniden deneme ve ters sırayla dönen istekler.
- Sohbet: taslaklar, alıntılar, tepki/düzenleme/sabitler, arama, kanal yalıtımı, aynı nonce ile yeniden deneme, yukarıda okurken yeni mesaj ve okundu/odak durumları.
- Hesap: DPAPI kayıt/yeniden açma, çevrimdışı bağlanma, token yenileme/iptali, beni hatırla kapalı ve çıkış/yenileme yarışı.
- Ses durumları: iptal edilen katılımın sunucuda temizlenmesi ve eski hesabın/geç oturumun yanıtlarının uygulanmaması. HTTP ve kontrol fixture'ları kullanıldı.
- Özellik/yerel veri testleri: tema, büyük dosya sınırları/iptal, yol koruması, geçmiş, CSV, oyun kısayolu, kapak/favori ve kullanıcı verileri.
- Kurulum: gömülü dosyalar/özetler, simge/kısayol, yeniden kurulum ve veri koruma.
- Patch: RSA, dosya özetleri, bozulmuş paket/yol taşması/eski sürüm reddi, uygulama/geri alma/veri koruma. 2.1, 4.3 ve 4.7 güncelleyicilerinden 4.8 kurulumu doğrulandı.
- Kaspersky: son uygulama, kurulum, güncelleyici ve patch; 36 nesne, 0 tespit, 0 şüphe, 0 hata.

## Açık sınırlar

Ses/medya uygulaması 4.7 ile aynıdır. Farklı ağlarda gerçek mikrofon ve ekran seçimi testi tamamlanmadı. TURN/SFU yok; ses beta 6 kişi ve tek paylaşımla sınırlıdır. KLIPY üretim erişimi, Spotify OAuth ve güvenilir Windows yayıncı sertifikası henüz yoktur. Mesajlarda uçtan uca şifreleme bulunmaz.

Bu rapor bütün hataların bittiği veya tüm güvenlik ürünlerinin dosyayı kabul edeceği iddiası değildir. Tasarım araştırmasının kaynakları DESIGN-REFERENCES.md dosyasında listelenir.