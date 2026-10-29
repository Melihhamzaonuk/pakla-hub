# Pakla Hub 4.21.1 — 29 Ekim 2026

## Bu sürüm

- 17 kısa, özgün ve yerel işlem sesi: katılma/ayrılma, diğer katılımcılar, mikrofon, sesi kapatma, kamera, ekran paylaşımı, mesaj/arama ve kayıt/klip. Genel ses düzeyi ile görüşme/mesaj/klip kategorileri ayrı kapatılır. Varsayılan düzey %35; susturulmuş sohbetler bildirim sesi üretmez. Sesler görüşme akışına karıştırılmaz; işletim sisteminin varsayılan çıkışından çalınır. Gelen arama sesi kısa bir işarettir, sürekli zil değildir.
- Sekiz ekran paylaşımı hedefi: 480p/15, 720p/10, 720p/15, 720p/30, 1080p/15, 1080p/30, 1080p/60 ve 1440p/30. Kaynak değiştirme iptal edilirse eski yayın korunur. Kalite canlı değişir; hedef bitrate katılımcılar arasında paylaştırılır. Gerçek kalite kaynak, cihaz ve ağ kapasitesiyle sınırlıdır. Ekran sesi bu sürümde yoktur.
- Hafif çalışma ve azaltılmış hareket. Odak kaybında dekoratif animasyon zamanlayıcıları durur; sistem ölçümü arka planda 10 saniyeye, UI özeti 15 saniyeye, Discord aktivite kontrolü 60 saniyeye seyrekleşir. Gelen arama kontrolü arkada 5 saniyedir. Aktif görüşme kalp atışı ve kullanıcı tarafından başlatılmış kayıt sürer. Sohbet ekranlarından ayrılıp arka planda 60 saniye boş kalan, aktif görüşmesi bulunmayan ses görünümü serbest bırakılır. Sayısal CPU/RAM tasarrufu için farklı donanımlarda karşılaştırmalı ölçüm yapılmadı.
- DM ve topluluk geçmişinde aşağıda kalmayan kullanıcıya “Son mesaja git” düğmesi. Önceki kanal oluşturma, kategori/rol/kişi izinleri, mesaj taslakları ve susturma akışları korunur.
- Uygulama içinde yerel klip oynatıcı ve başlangıç/bitiş saniyesiyle kırpılmış yeni kopya. Orijinal dosya korunur; otomatik yükleme yoktur. Oynatıcı sadece seçilmiş MP4'ü istek aralıklarıyla okur; bütün klip belleğe alınmaz. Harici gezinme, indirme, kamera/mikrofon ve host nesneleri kapalıdır. Kayıt uzunluğu seçenekleri 10/15/30/45/60/90 saniyedir. 256 MB tampon ve 10 saniyelik parçalar nedeniyle gerçek eldeki süre daha kısa olabilir; parçalar arasında kesinti olabilir.

## Güvenlik

AbuseGuard.sql, mesaj ekleme/düzenleme için hesap başına ortak 20/10 saniye bütçe; arkadaşlık isteğinde 10/dakika ve arama başlatmada 6/dakika sınırı ekler. Önceki DM ve topluluk sınırları ayrıca sürer. Sayaç güncellemesi tek satırlık atomik UPSERT kullanır. Sayaç tablosu RLS ile kapalıdır; istemciye tablo/yardımcı işlev yetkisi verilmez. Gerçek kullanıcı verisi temizlenmez.

Turnstile sayfası yalnızca doğrulama yapar; e-posta/şifre toplamaz. Uygulama origin denetimiyle aldığı tek kullanımlık kanıtı Supabase Auth'a gotrue_meta_security.captcha_token alanında gönderir. Kanıt diske kaydedilmez; tekrar kullanılamaz. Refresh token akışı CAPTCHA istemez. Gizli Turnstile anahtarı yalnızca Supabase ayarında tutulur, istemci/yayın paketine girmez. Sunucu CAPTCHA aktivasyonu ve canlı doğrulamanın kesin durumu release-verification.json dosyasındadır. Zorunlu koruma açıldıktan sonra eski sürümler yeniden giriş için güncellenmelidir.

Bu önlemler tam DDoS veya sıfır veri sızıntısı garantisi değildir. Cloudflare'daki doğrulama sayfası tüm Supabase API trafiğini proxy etmez. Ağ seviyesinde WAF, ek kapasite, izleme/uyarı, bağımsız güvenlik incelemesi ve yedek geri dönüş tatbikatı hâlâ gereklidir. Mesajlar uçtan uca şifreli değildir. SMTP/service_role/patch özel anahtarı istemciye eklenmez.

## Testler

- Derleme ve sahte HTTP ile kanal/rol/izin, modal doğrulama, hata sonrası formun korunması, kayıt-yenileme yarışı, 344–1440 mantıksal genişlikler ve %150 ölçek.
- DM araması sohbet içinde kalır; davet, kabul, karşı tarafın sonlandırması, ayrılma, bildirim susturma ve hesap ayrımı yeniden sınandı.
- Gerçek WebView2 + sahte cihazlarla izin verme/reddetme. İki yerel gerçek WebRTC istemcisi arasında sentetik ses/kamera/ekran, yeniden bağlantı ve iz temizliği. Kişisel mikrofon/kamera/ekran kullanılmadı.
- JS testleri sekiz kalite profilini, encoder bitrate/FPS sınırını, iptal edilen kaynak seçimini, geç izin ve cihaz bitişi yarışlarını doğrular. İşlem sesleri başarı olaylarında üretilir.
- 17 PCM sesinin başlık/uzunluk ve sıfır ses düzeyi kontrolü; gerçek hoparlöre test sesi verilmedi. Animasyon zamanlayıcısının durması/devam etmesi, boş renderer temizliği ve arka plan sorgu aralıkları sınandı.
- Gerçek Windows medya motoruyla dört saniyelik renkli fixture videodan 1–3 saniye aralığına ait iki saniyelik yeni klip ve thumbnail üretildi; orijinal SHA-256 değişmedi. Geçersiz/NaN/süre dışı aralıklar reddedildi. Yerel önizleme gerçek WebView2'de sessiz oynadı, zaman ilerledi ve durakladı.
- Gerçek Turnstile widget'ı hem tarayıcıda hem uygulamanın WebView2 penceresinde otomatik doğrulandı. Sahte HTTP testi eksik/yeniden kullanılan kanıtı reddetti; yenilemenin etkilenmediğini doğruladı. Canlı Auth doğrulaması ayrı kayıt altına alınır.
- Sunucuda transaction içinde geçiş iki kez uygulandı, ortak bütçe/hesap ayrımı/süre yenilenmesi/tekrar deneme ve kapalı yardımcılar sınandı, fixture kayıtları geri alındı. Sonra doğrulanmış geçiş canlıya uygulandı.

## Açık işler

Herkese açık klip akışı, bulut klip yükleme/moderasyon, büyük ölçekli arama, TURN/SFU, mobil istemci, oyun olayıyla otomatik klip, ekran sesi, Spotify OAuth ve Authenticode sertifikası tamamlanmadı. Topluluk özellikleri Discord ile eşit değildir. Kişisel cihazlar, farklı ağlar ve altı kişilik görüşme yükü ayrıca denenmelidir. Kaynak kod paketi özel taslaktır; yeniden kullanım lisansı seçilmedi.

## Araştırmada örnek alınanlar

[Discord işlem sesleri](https://discord.com/blog/how-to-manage-your-discord-desktop-notifications): olay bazında ses kontrolü. [Medal kayıt ayarları](https://support.medal.tv/support/solutions/articles/48001271487-getting-to-know-medal-s-settings): kalite/performans seçimi, kısayol ve klip yönetimi. [Supabase CAPTCHA](https://supabase.com/docs/guides/auth/auth-captcha), [Cloudflare WebView entegrasyonu](https://developers.cloudflare.com/turnstile/get-started/mobile-implementation/) ve [Microsoft medya kırpma](https://learn.microsoft.com/en-us/windows/uwp/audio-video-camera/media-compositions-and-editing): sağlayıcıların resmî akışları. Rakiplerin marka/ikon/ses dosyaları kopyalanmadı.

4.21.1: dar ayar kartındaki açıklama kısaltıldı ve sayfa başlığı sadeleştirildi. 4.21 davranış testleri geçerlidir; 4.21.1 derleme/kurulum/patch kontrolleri ayrıca çalıştırılır.
