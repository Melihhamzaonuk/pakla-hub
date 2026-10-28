# Pakla Hub 4.19 — topluluklar

Kanal, kategori ve rol kaydını etkileyen JSON biçim hatası giderildi. İç içe nesneler sunucuya anahtar/değer dizisi yerine JSON nesnesi olarak gönderilir; profil alan adları ve rol dizileri korunur. Kategori izinleri, eşitleme ve yönetim geçmişi için eksik istemci işlem izinleri tamamlandı.

- Topluluk ve sohbet ekranlarında tek sunucu şeridi; Pakla'nın diğer bölümlerine üst bölüm menüsünden geçiş.
- Kompakt sunucu başlığı ve açılır menü: genel bakış, okundu işaretleme, bildirimler, davet, kanal/kategori oluşturma ve ayarlar.
- Açık “Kanal oluştur” düğmesi, kategori yanında +, kanal yanında düzenleme düğmesi.
- Metin, duyuru ve ses kanalı oluşturma/düzenleme. Hata halinde form ve girilen bilgiler korunur; aynı kayıt isteğini tekrar denemek ikinci bir kanal oluşturmaz.
- Yeni özel kanal, izinleriyle kanal çoğaltma, yukarı/aşağı sıralama, arşivleme ve geri açma.
- Kanal başına yavaş mod. Kurucu/yönetici muafiyeti ve mesaj tekrar denemelerinde aynı mesaja izin verilir.
- Daha kompakt rol/kişi kanal izinleri; kategori eşitlemesi çalışır.
- Arka plan sorgusuyla kanal kaydı çakıştığında eski sonuç yeni seçimi silemez; başarılı kayıttan sonra liste tekrar alınır.

Sunucu geçişi uygulanmıştır. Kurucu, yönetici veya “Kanalları yönet” yetkili rolü yeni kanal açabilir. Normal üyeler sunucu sahibinden bu yetkiyi almalıdır; yetki kontrolleri sunucuda da yapılır.

Bu sürüm Discord'un bütün özelliklerini içermez. Forum/thread, Stage, etkinlikler, AutoMod, bot/webhook platformu, ayrıntılı sunucu yetkileri, gelişmiş davet yönetimi ve büyük ölçekli medya altyapısı tamamlanmadı. Ses/görüntü/ekran paylaşımı beta sınırları sürer. Ayrıntılar QUALITY-REPORT.md ve TOPLULUK-YOL-HARITASI.md içindedir.
