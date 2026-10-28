# Pakla Hub 4.18 — doğrulama ve sınırlar

28 Ekim 2026. Bu sürüm ana ekran, uygulama gezinmesi, sohbet başlıkları/yazma alanı, sağ tık menüleri ve yüksek DPI davranışını yeniler.

## Kontrol edilenler

- 344, 600, 780, 1024 ve 1440 mantıksal genişlikte ana sayfa, sohbet, topluluk, klipler, kitaplık, araçlar ve ayarlar kontrol edildi. %100 ve %150 test ölçeği kullanıldı. En küçük pencere ölçüsü Windows'un çerçevesi ve uygulamanın minimum boyutuna göre yuvarlanır.
- Üst menü eylemlerinin çakışmaması, görünür gezinme düğmelerinin sınırlar içinde kalması, dar ekranda bölüm menüsü, geniş ekranda sol gezinme ve sohbetlerde kompakt şerit doğrulandı.
- Kalıtılan, önceden biçimlendirilmiş yazı tipinin ikinci kez büyütülmesi için regresyon testi eklendi; tasarım punto değeri korunuyor.
- Ctrl+1–6 bölüm değişimi, geri/ileri geçmişi, GIF eylemi, mesaj gönderme/yeni satır açıklaması ve koyu menü çizicisi doğrulandı. Örnek verili gerçek WinForms ekranları oluşturuldu; önizlemeler tasarım maketi değil, uygulama kontrollerinden alınan test görüntüleridir.
- Çoklu rol gönderiminin gerçek istemci serileştirmesi, izin düzenleyicisinde bekleyen değişikliklerin korunması, kategori eşitleme kilidi ve eşitlemeyi kaldırma tekrar test edildi.
- Değişmeyen üye panelinin tekrar oluşturulmaması, rol/kanal düzenleme ve önceki responsive kontrol testleri geçti.
- Genel self-test 17 gezinme/araç sayfasını ve yerel veri korumalarını kontrol etti. Gerçek oyunlara veya DNS ayarlarına değişiklik yapılmadı.
- Kurulum self-test'i geçici dizinde yük çıkarma/hash, kısayol/simge ve yeniden kurulumda kullanıcı verisini korumayı sınadı. Kişisel kurulum değiştirilmedi.
- Patch testleri RSA imzası, dosya hash'leri, bozulma ve yol atlama saldırısı reddi, eski sürüm reddi, uygulama, hata halinde geri alma ve kullanıcı verisini korumayı kapsar.
- Özgün 2.3.0 güncelleyicisiyle 4.18 geçişi ayrıca doğrulandı. Kullanıcı kütüphanesi ve sürüm geçmişi korundu.

4.16/4.17 sunucu izin geçişleri bu sürümden önce uygulanmıştır. Bu turda veritabanı şeması değiştirilmedi. 4.18 yeni rol/kanal izinleri ile cihaz kontrollerini içerir.

## Devam eden sınırlar

Ses/görüntü/ekran paylaşımı beta: en fazla altı kişi, aynı anda bir ekran paylaşımı. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. İki WebView2 ile sentetik medya, yeniden bağlantı ve iz temizliği doğrulandı; altı kişilik yük, gerçek kişisel mikrofon/kamera ve farklı ev/kurum ağı testleri tamamlanmadı.

Rol oluşturma/atama kurucuda kalır; tam rol yönetim delegasyonu, forum/thread, AutoMod, gelişmiş moderasyon ve büyük ölçekli medya altyapısı tamamlanmadı. Eski çekirdeğin ek moderasyon korumaları da sürer.

KLIPY ortak test kotası 100 çağrı/saat. Spotify OAuth yapılandırılmadı. Mesajlar uçtan uca şifreli değildir. Windows Authenticode yayıncı sertifikası yok; patch'in RSA-SHA256 imzası ayrı bir mekanizmadır. FPS, internet hızı veya tüm antivirüslerde sıfır uyarı garantisi verilmez.

Kaynak kod yayını taslağı ayrı tutulur; uygulama güncellemesini yayımlamak kaynakları halka açmaz. Lisans, bağımsız güvenlik incelemesi, sıfırdan sunucu kurulumu ve CI çalışmaları devam eder.

