# Pakla Hub 4.23.0

Durum: Kurulum ve RSA imzalı patch 4.23.0 genel güncelleme kanalında yayımlandı. Dağıtım dosyaları indirilerek hash değerleri doğrulandı. Yayın işlemi kurulu kullanıcı kopyasını veya hesap verilerini değiştirmez.

## Düzeltilenler ve değişen akışlar

- Pakla Clean ana pencereye gömüldü. Aktif temizlik bitmeden veya iptal tamamlanmadan gezinme engellenir.
- Profil, GIF seçici, sunucu/rol/kanal/izin düzenleyicileri aynı Hub penceresinin içinde açılan panelleri kullanır. Sonuç ve taslak korunur; alttaki gezinme panel açıkken çalışmaz. Gelen arama bildirimi ile Windows dosya seçicileri kendi amaçlarına uygun bildirim/diyalog olarak kalır.
- DM ve toplulukların ortak mesaj bileşeni görünür GIF'leri otomatik yükler. Küçük KLIPY kaynağı önceliklidir. Doğrudan katalog ve CDN kontrolü başarılı: gerçek 90×90 GIF indirildi.
- GIF bayt önbelleği en fazla 12 MB/20 kayıt; aynı görsel yeniden indirilmez. Aynı anda iki indirme; görünür olmayan görsellerin çözümlenmiş görüntüleri bırakılır. GIF 4 MB ve boyut/kare sınırlarına tabidir. Arka planda veya hareket azaltıldığında durağan kare kullanılır. Hata durumunda yeniden deneme görünür.
- Topluluklarda yeni sunucu kapağı, mevcut kapaklara oran korumalı kırpma ve daha düzenli kanal alanı. Kategori aç/kapat artık tüm sohbet ekranını yeniden yaratmaz. Aynı kanala yeniden tıklamak ekranı sıfırlamaz. Kanal oluşturma, rol/kategori/üye izinleri korunur.
- Medal'ın kütüphane → klip seçme → önizleme/kırpma → yeni kopya akışından yararlanılarak uygulama içi klip stüdyosu kuruldu. Oynatıcı, sürüklenebilir zaman çizgisi, saniye alanları, aralığı izleme, başlık/koleksiyon ve dışa aktarma aynı çalışma alanında.
- Orijinale dokunmadan kırpılmış kopya oluşturulur. MP4 içe aktarma gerçek süreyi okur ve dosyayı kütüphaneye kopyalar. Sınır: işlem başına 8 dosya, dosya başına 200 MB/10 dakika; değişmekte olan kaynak reddedilir.
- Kitaplıkta mevcut 24 kartlık sayfalama korundu. Arama yazılırken 220 ms beklenerek her tuşta görsel bileşenlerin yeniden oluşturulması azaltıldı.
- Pakla'nın kendi logosu etrafında yörünge hareketi, hafif salınım ve gerçek indirme ilerlemesi kullanan özgün açılış ekranı. Hareket azaltma tercihine uyar. Ana pencere varsayılan olarak büyütülmüş açılır; tercihi değiştirilebilir.
- Kurulu sürüm açılışta güncellemeyi kontrol eder, indirir; SHA-256, RSA imzası ve sürüm eşleşmesi doğrulandıktan sonra mevcut güncelleyiciyle yükler. Ağ/indirme hatasında mevcut sürüm açılır; bekleme atlanabilir. Taşınabilir kopya otomatik kurulmaz. Güncelleme için tüm Hub yönetici olarak çalıştırılmaz.

## Doğrulama

- Uygulama/kurulum self-test ve patch self-test: geçti. Hash/imza, bozuk paket/yol aşımı/sürüm düşürme reddi, uygulama/geri alma ve veri koruma.
- Özgün 2.3.0 güncelleyici 4.23 paketini doğrulayıp izole klasöre uyguladı; kitaplık ve sürüm kaydı korundu.
- Açılış doğrulama hattı gerçek imzalı 4.23 paketiyle, 4.22 kuruluymuş gibi test edildi. Bozulmuş indirme ve feed/manifest sürüm uyumsuzluğu reddedildi. Canlı kurulum değiştirilmedi.
- Temizlik/paneller için yeni üst düzey pencere açılmadığı, kabul sonucu/taslak korunması ve panel sırasında gezinme engeli test edildi.
- GIF işaretleyici, otomatik yükleme, gerçek görüntü bileşeni, önbellek tekrar kullanımı ve hareket azaltmada durağan kare: geçti. Sentetik aktarım kullanıldı; gerçek katalog/CDN ayrıca kontrol edildi.
- Gerçek Windows medya işlemleriyle 4 saniyelik sentetik MP4 içe aktarıldı ve 1–3 saniye kırpılarak 2 saniyelik kopya üretildi. Kaynağın hash'i değişmedi.
- Gerçek WebView2 oynatıcıda 1–2 saniye aralığına atlama, oynatma ve bitişte durma: geçti. Ses kapalı, sentetik renkli kareler; kişisel klip veya cihaz kaydı yapılmadı.
- 344/600/780/1024/1440 genişlik, %100 ve %150 DPI kontrolleri: kabuk/başlık sınırları, kısayollar, geri/ileri, sunucu ve sohbet görünümü.
- Sunucu testleri: kanal/kategori oluşturma, hata sonrası formu koruma/yeniden deneme, yeni kanalı seçme, yenileme yarışları, çoklu rol, üye istisnaları, kategori eşitleme ve kaldırma, yetkisiz işlemleri gizleme.
- DM testleri: susturma/hesap ayrımı, satır içi arama başlatma, kabul/bitirme, uzaktan reddetme; gerçek mikrofon/kamera açılmadı.
- Önceki ses, CAPTCHA, arka plan yenileme ve boş ses görünümü kontrolleri geçti.

Test kanıtları `work/v423/` içinde; önemli sonuçlar bu klasördeki `*-test-result.txt` dosyalarına kopyalanmıştır.

## Sınırlar

Bu sürüm Discord veya Medal'ın bütün servislerini içerdiği iddiasını taşımaz. Klipler yereldir; herkese açık klip paylaşım sunucusu/feed'i eklenmedi. Uzun kayıt/montaj/otomatik oyun anı tanıma geliştirilmedi. Yeni bulut yetkisi veya veri tabanı şeması değişikliği yapılmadı.

Ses/görüntü bağlantılarının mevcut TURN/SFU sınırı sürer. Önceki Game Boost/FPS özelliğinde Windows ETW izni gereksinimi değişmedi. Authenticode yayıncı sertifikası yoktur; RSA patch imzası ayrı mekanizmadır.

## Tasarım için incelenen birincil kaynaklar

- [Medal: başlangıç, kütüphane ve hızlı işlemler](https://support.medal.tv/support/solutions/articles/48000959661/)
- [Medal: kırpma ve düzenleyici akışları](https://support.medal.tv/support/solutions/articles/48001211535/)
- [Medal: klip içe aktarma](https://medaltv.freshdesk.com/support/solutions/articles/48001210933-how-to-import-clips-into-medal)

Marka/mascot kopyalanmadı; Pakla'nın logosu ve bileşenleri kullanıldı.
