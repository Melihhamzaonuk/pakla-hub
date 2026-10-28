# Pakla Hub 4.19

Ekibin, anların ve araçların. Windows x64 masaüstü uygulaması.

[Windows için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar **Ayarlar → Güncellemeler → Güncelleme ara** yolundan 4.19.0'a geçebilir. Bildirimler açıksa açılış kontrolü yeni sürümü duyurur; yükleme kullanıcı seçimiyle başlar.

## Topluluklar yeniden düzenlendi

Tek sunucu şeridi, kompakt sunucu başlığı ve açılır yönetim menüsü. Görünür Kanal oluştur düğmesi, kategori yanında + ve kanal yanında ayarlar bulunur. Pakla'nın diğer bölümlerine üst bölüm menüsünden geçilir.

![Topluluk görünümü — gerçek arayüz, örnek test verileri](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.19.0/Pakla-Topluluk.png)

Kanal, kategori ve rol kaydındaki iç içe JSON biçim hatası giderildi. Kategori izinleri, eşitleme ve yönetim geçmişinin eksik istemci çağrıları tamamlandı. Kanal kaydı başarısız olursa form ve bilgiler korunur; aynı oluşturma isteği tekrar denendiğinde ikinci kanal oluşmaz. Kayıt sonrası eski arka plan sorgusunun yeni seçimi silmesi düzeltildi.

Metin, duyuru ve ses kanalları; özel kanal oluşturma, izinleriyle çoğaltma, yukarı/aşağı sıralama, arşivleme/geri açma ve sunucuda uygulanan yavaş mod desteklenir. Kurucu/yönetici veya Kanalları yönet yetkili rolü kanal açabilir. Normal üyelerin bu yetkiyi sunucu sahibinden alması gerekir.

Çoklu roller, rol renkleri/sırası, kişi ve rol bazlı kanal istisnaları, canlı kategori izin mirası, moderasyon hiyerarşisi, bildirimleri sessize alma ve toplu okundu işaretleme bulunur. Rol oluşturma/atama kurucuda kalır.

Sohbet, GIF, arkadaş grupları, DM görüşme davetleri, klipler, kütüphane, yerel müzik, temizlik ve bağlantı araçları korunur. Temizlik kullanıcı seçimiyle yapılır; FPS veya internet hızı artışı garanti edilmez.

## Geliştirme durumu

**Discord özellik eşitliği tamamlanmadı.** Forum/thread, Stage, etkinlikler, AutoMod, bot/webhook platformu, ayrıntılı rol delegasyonu ve büyük ölçekli medya altyapısı devam eden işlerdir.

Ses/görüntü/ekran paylaşımı beta: en fazla altı kişi ve aynı anda bir ekran paylaşımı. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. Gerçek kişisel cihazlar, farklı ağlar ve altı kişilik yük testleri tamamlanmadı. KLIPY ortak test kotası 100 çağrı/saat; Spotify OAuth yapılandırılmadı. Mesajlar uçtan uca şifreli değildir. Windows yayıncı sertifikası yok; patch paketleri ayrı RSA-SHA256 imzasıyla doğrulanır.

[Doğrulama raporu](distribution/4.19.0/QUALITY-REPORT.md) · [Sürüm notları](distribution/4.19.0/RELEASE.md) · [Topluluk kapsamı ve yol haritası](distribution/4.19.0/TOPLULUK-YOL-HARITASI.md)

Destek: supportpakla@gmail.com
