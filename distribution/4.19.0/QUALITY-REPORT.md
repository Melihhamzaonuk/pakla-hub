# Pakla Hub 4.19 — doğrulama ve sınırlar

28 Ekim 2026. Odak: toplulukların çalışır kanal/rol yönetimi ve daha kompakt kullanım.

## Düzeltilen kök nedenler

1. İç içe Dictionary değerleri JSON nesnesi yerine `[{"key":…, "value":…}]` biçiminde gidiyordu. Kanal, kategori ve rol işlemlerindeki `p_data` bu yüzden sunucunun sözleşmesiyle uyuşmuyordu. Yeni dönüştürücü nesne, dizi, null ve DataMember alan adlarını ayrı korur. Kayıt/oturum metadata'sındaki `display_name`, `handle` gibi adlar için regresyon kontrolü vardır.
2. Kategori izinleri, kategori eşitleme ve denetim geçmişi RPC'leri istemci izin listesinde yoktu. Gerçek CloudAccount.Rpc üzerinden HTTP katmanına ulaştıkları kontrol edildi.
3. Arka plan sorgusu sürerken zorlanan yenileme atlanabiliyordu. Ayrıca eski sorgu yeni kanal seçimini temizleyebiliyordu. Sorgular sıraya alınır; eski nesil sonuçlar uygulanmaz.
4. Asenkron kanal düzenleyicisinin UI iş parçacığına dönüşü açık hâle getirildi. Hata form üzerinde gösterilir; içerik korunur. Kaydetme tamamlanmadan pencere kapanmaz.

## Test edilenler

- Gerçek derlenmiş istemci, sahte HTTP hedefi ve sentetik kullanıcılarla: kanal formu, geçersiz ad reddi, servis hatası, bilgilerin korunması, aynı nonce/payload ile tekrar deneme, metin/ses/özel kanal yükü, kategori kaydı ve kayıt sonrası listede yeni kanalın görünmesi.
- İç içe JSON nesnesi/dizisi, rol dizisi, nullable izin ve profil metadata alan adları; önceki alan-adı aramaları yerine JSON yapısı ayrıca denetlendi.
- Açık kanal düğmesi, kategori +, kanal ayarları; 344/600/780/1024/1366/1440 mantıksal genişlikler. %100 ve %150 ölçek denetimleri. Pencere alt sınırı Windows çerçevesine göre yuvarlanır.
- Rol ve kişi izinleri, bekleyen izin değişikliğinin korunması, eşitleme kilidi ve eşitlemeyi kaldırma; çoklu rol gönderimi, alt yetkili kanal yöneticisi ve normal üye görünürlüğü; yönetim diyaloglarının gerçekten açıldığına dair sayaçlı kontroller.
- Mevcut DM ve görüşme testleri: davet, kabul, otomatik katılım, kapatma, sessize alınmış aramanın reddi; bildirim ve sabit tercihlerinin hesaplar arasında ayrılması. Gerçek mikrofon/kamera/ekran açılmadı.
- Canlı sunucuda transaction içinde iki kez şema geçişi, kanal oluşturma ve yeniden listeleme, tekrar denemede tek kayıt, nonce uyuşmazlığı reddi, özel ses kanalı ve kopyasının gizliliği, sıralama, yavaş mod, aynı mesajın idempotent tekrarı, alt yetkili kanal yöneticisi, kategori eşitleme, geçmiş ve toplu okundu. Yetkisiz ve doğrudan tablo erişimi reddedildi. Sentetik kullanıcılar ve kayıtlar geri alındı; gerçek kullanıcı kanalları kullanılmadı.
- Aynı sunucu geçişi sonrasında canlı ortama uygulandı. Kanal/rol düzenlemelerinin yetkilendirmesi sunucu tarafında korunur.
- Genel uygulama ve kurulum kontrolleri geçici dizinlerde yapılır; kişisel kurulum değiştirilmedi. Patch doğrulaması imza, hash, bozulma, yol atlama, downgrade reddi, uygulama, geri alma ve kullanıcı verisinin korunmasını kapsar.

Ekran görüntüleri gerçek WinForms kontrollerinden, örnek test verileriyle alınmıştır; kişisel sohbetler kullanılmamıştır. Dağıtım doğrulamasının son durumu release-verification.json içindedir.

## Sınırlar

Discord özellik eşitliği tamamlanmadı. Ayrıntılı liste TOPLULUK-YOL-HARITASI.md içindedir. Rol oluşturma ve atama kurucuda kalır; diğer kullanıcılara kanal/görünüm/yönetici yetkisi verilebilir. Sunucu başına önceki 20 aktif kanal ve 12 kategori/rol sınırları sürer; kapasite artırımı yük testleri gerektirir.

Ses/görüntü/ekran paylaşımı beta: en fazla altı kişi ve aynı anda bir ekran paylaşımı. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. Gerçek kişisel cihazlar, farklı ağlar ve altı kişilik yük testleri tamamlanmadı.

KLIPY ortak test kotası 100 çağrı/saat. Spotify OAuth yapılandırılmadı. Mesajlar uçtan uca şifreli değildir. Windows Authenticode yayıncı sertifikası yok; patch RSA-SHA256 imzası ayrı bir mekanizmadır. FPS, internet hızı veya bütün antivirüslerde sıfır uyarı garantisi verilmez.

Kaynak kod paketi özel taslaktır. Lisans, bağımsız güvenlik incelemesi ve sıfırdan tüm sunucu kurulumu doğrulaması tamamlanmadı. Bu güncelleme kaynak kodunu halka açmaz.
