# Pakla Hub 4.10 güvenlik notları

4.10.0 son dosyaları Kaspersky 21.26 ile tarandı: 36 nesne, 0 tespit, 0 şüphe, 0 hata. Son dosyaların SHA-256 değerleri release-verification.json, yerel tarama sonucu antivirus-report.txt içindedir. Sonuç bu dosyalar ve tarama anı içindir; tüm güvenlik ürünleri için garanti değildir.

Bu derleme **Authenticode imzalı değildir**. RSA-SHA256 patch doğrulaması Windows'un güvenilir yayıncı imzasından ayrıdır. Bilgisayarda kullanılabilir bir kod imzalama sertifikası bulunmadığından yayıncı imzası oluşturulmadı. Yeni veya imzasız dosyalarda SmartScreen itibar uyarısı çıkabilir.

Uygulama yönetici yetkisi istemeyen `asInvoker` manifesti taşır. Paketleyici veya gizleme katmanı kullanılmaz. Kurulum kullanıcı hesabına yapılır. Otomatik başlangıç kaydı, antivirüs istisnası, güvenlik ürünü kapatma veya güvenlik denetimi atlatma özelliği eklenmez. Kullanıcı onaylı Windows kaldırma kaydı dışında sistem geneline kurulum yapılmaz. İmzalı patch'ler kendi uygulama dosyalarını günceller; kullanıcı verilerini korur.

## Güvenilir yayıncı imzasıyla derleme

Windows SDK SignTool ve güvenilir bir otoriteden alınmış, bu Windows kullanıcısının `My` sertifika deposunda özel anahtarı erişilebilir bir kod imzalama sertifikası gerekir. Kendi ürettiğin bir sertifika, herkese açık dağıtımda güvenilir yayıncı sağlamaz.

`Build.ps1` parametreleri: `SigningCertificateThumbprint`, `SignToolPath`, isteğe bağlı HTTPS `TimestampServer`. Derleme güncelleyiciyi imzalar, uygulamaya ekler, uygulamayı imzalar, kuruluma ekler ve kurulumu imzalar. SHA-256 ve RFC 3161 zaman damgası kullanılır. Yayıncı imzası veya zaman damgası doğrulanamazsa derleme durur. Ardından `Make-Release.ps1` ile patch ve son dosya özetleri üretilir. İmzalandıktan sonra dosyaları değiştirme. Özel sertifika/anahtarları dağıtım paketine veya depoya koyma.

İmzalama dalı bu bilgisayarda sertifika bulunmadığı için gerçek bir sertifikayla çalıştırılıp doğrulanmadı.

## Yanlış tespit bildirimi

Gerçek bir malware tespiti oluşursa tespit adını, ürün/veritabanı sürümünü ve aynı SHA-256 değerine sahip ilgili dosyayı üreticinin resmi inceleme kanalına gönder. SmartScreen'in düşük indirme itibarı uyarısı malware tespitiyle aynı şey değildir. Antivirüs korumasını kapatmak veya kullanıcılara topluca istisna ekletmek dağıtım çözümü olarak kullanılmaz.

- [Microsoft: SmartScreen ve uygulama itibarı](https://learn.microsoft.com/windows/apps/package-and-deploy/smartscreen-reputation)
- [Microsoft: Yanlış tespit incelemesi](https://www.microsoft.com/en-us/wdsi/filesubmission)
- [Microsoft: SignTool](https://learn.microsoft.com/en-us/windows/desktop/seccrypto/signtool)

## Arkadaşlık ve mesaj erişimi

Arkadaş profili kullanıcı tarafından etkinleştirilir. E-posta adresleri sosyal tablolara kopyalanmaz. Mesajlar sunucuda saklanır ve uçtan uca şifreli değildir. RLS ile yalnızca mesajın gönderen/alıcı hesapları okuyabilir. Anonim rolün tablo/RPC erişimi yoktur; istemcilere doğrudan yazma izni verilmez. RPC fonksiyonları kullanıcıyı auth.uid() ile belirler; security definer fonksiyonları boş search_path kullanır. Arkadaşlık, engel, boyut ve hız sınırları sunucuda doğrulanır. Gönderim nonce değeri yeniden denemede aynı mesajın çoğalmasını önler. Taslaklar yalnızca bellekte tutulur ve hesap değişiminde temizlenir.

Üç geçici kullanıcıyla transaction/rollback içinde yetki, istek kabulü, özel mesaj okuma, okundu, engelleme ve hız testleri çalıştırıldı; test kullanıcıları kalıcı olarak oluşturulmadı. Gerçek hesap oturumuyla sosyal durum RPC'si ve arkadaş olmayan kullanıcıya geçmiş erişiminin reddi doğrulandı. Gerçek kişilere test mesajı gönderilmedi.

## Ekran ölçeği ve kurulum

.NET Framework 4.8 PerMonitorV2 kullanılır. Kurulum uygulamaya ait PaklaHub.exe.config dosyasını yazar; eski üç dosyalı patch sisteminden gelen güncellemede uygulama bu sabit yapılandırmayı ilk açılışta tamamlayıp kendisini bir kez yeniden başlatır. Yeni bir servis, yönetici yetkisi veya otomatik başlangıç kaydı eklenmez. Kaldırıcı bu yapılandırmayı da temizler.

## Topluluk ve medya alanları

Topluluklar davetli ve üyelik kontrollüdür. Yeni tablolar RLS ile korunur; doğrudan kanal mesajı okuma/yazma yetkileri kapalıdır. Üyelik, rol, kanal ve arşiv durumları RPC içinde doğrulanır. Süreli/sınırlı davetler, nonce ile yeniden deneme ve gönderim hız sınırları sunucudadır. Üç geçici kullanıcıyla transaction/rollback testleri geçti; deneme kullanıcısı kalmadı. Özel sohbet ve arkadaş profil yetki testleri de geçti.

Banner ve avatarlar yeni JPEG bitmaplerine dönüştürülüp boyutları sınırlanır. Discord aktivitesi varsayılan olarak kapalıdır; yalnızca sabit, genel durum metinleri gönderilir. Bot tokenı veya Discord parolası alınmaz. Bu bilgisayarda uygulama kimliğiyle handshake ve yalnızca test işleminin boş aktivite temizleme komutu doğrulandı; test sırasında aktivite yayımlanmadı.

Müzik yalnızca kullanıcının seçtiği yerel MP3/WAV dosyalarını Windows ses motoruyla oynatır. Dosya yolları/parça adları Discord veya Pakla sunucusuna gönderilmez. Sistem ses düzeyi yerine oynatıcı ses düzeyi ayarlanır.

## 4.3 kanal etkileşimleri

Tepki ve sabit tablolarında RLS açıktır; anonim ve oturum açmış istemci rollerinin doğrudan tablo erişimi yoktur. RPC kullanıcıyı auth.uid() ile belirler, etkin üyelik/kanal, karşılıklı engel ve mesaj durumunu sunucuda doğrular. Mesajı yalnızca yazarı düzenleyebilir; kurucu/moderatör başkasının mesajını düzenleyemez. Sabitleme kurucu/moderatör yetkisi gerektirir. Silinmiş mesajlar sabit kotasını tüketmez. Kullanıcı başına dakikada 30 etkileşim sınırı vardır; tepkiyi geri almak sayacı sıfırlamaz. Emoji ekle/çıkar komutları aynı değere tekrar uygulandığında durumu tersine çevirmez.

Arama sorgusu 2–80 karakterdir; literal alt metin araması kullanır, son 10.000 aday mesajdan en fazla 60 sonuç döndürür. Mesaj ek bilgisi isteği en fazla 60 kimlik kabul eder. Son transaction/rollback testi üyelik, engel, rol, düzenleme, sabit, bozuk kimlik, idempotent tepkiler ve hız sınırlarını doğruladı; üç geçici kullanıcıdan hiçbiri kalmadı. Arayüzde eski hesap/kanal yanıtları, bekleyen arama ve geçmiş yenilemesi, taslak koruma ve çıkış temizliği test edildi.
## 4.3 sunucu yapısı

Kategori ve rol tabloları RLS ile korunur; doğrudan istemci erişimi yoktur. RPC auth.uid(), etkin üyelik ve yönetici rolünü doğrular. Kurucu özel yönetim rolü oluşturup atayabilir. Yetki değiştirme/rol kaldırma ilgili üyelerin etkin rolünü aynı transaction içinde günceller. Başka sunucunun kategori/rol kimlikleri kabul edilmez. Keşfet varsayılan kapalıdır; mevcut sunucular kendiliğinden yayımlanmaz. Yalnızca kurucunun seçtiği tanıtım bilgileri listelenir. Mesajlar üyelik gerektirir. Kurallar katılımda yeniden doğrulanır; yasaklı üyeler geri katılamaz. Duyuru kanalına yazma sınırı sunucuda da uygulanır.

Transaction/rollback testleri kurucu/yönetici/üye sınırları, yetki verme/geri alma, kategori izolasyonu, duyuru, arşivden açma, özel Keşfet, değişmiş kurallar ve yasaklı katılımı doğruladı. Test kullanıcıları kalmadı. Önceki sohbet etkileşim güvenlik testleri de geçti.

## Kayıt ve simge

Monitör kaydı Windows DXGI Desktop Duplication kullanır; WGC'nin sarı monitör çerçevesi açılmaz. Windows korumalı içerik sınırları aşılmaz. Kayıt elle başlar ve tepside/uygulamada görünür kalır. Gerçek DXGI testi, yalnızca üstte tutulan uygulamaya ait test desenine kırpılmış kaynakla, ses/mikrofon kapalı çalıştı. Oyun veya başka uygulama içeriği test için kaydedilmedi. Pencere yakalama test yolu WGC kullanmayı sürdürür; ürünün monitör yolu DXGI'dır.

Simge uygulama/kuruluma gömülüdür. Yalnızca hedefi Pakla olan mevcut kısayollar sürümlü simge yoluna güncellenir. Başka kısayollar, Windows simge önbelleği ve Explorer işlemi değiştirilmez. Yeni servis/sürücü kurulmaz.

## Spotify web görünümü

Microsoft.Web.WebView2 1.0.4314.35 resmi NuGet paketindendir. Bileşenler uygulamada gömülüdür; çıkarılan dosyaların SHA-256 değerleri yüklemede kontrol edilir. Microsoft lisans/NOTICE metinleri dağıtılır. Cihazda Edge WebView2 Runtime gerekir.

Üst düzey görünüm yalnızca resmi Spotify HTTPS adreslerini açar. İndirme, kamera/mikrofon/konum izni, host objects, web mesajları, parola otomatik kaydı ve geliştirici araçları kapalıdır. Liste/parça bağlantıları doğrulanır; paylaşım sorgu parametreleri atılır. Pakla çerez/parolaları okumaz veya Supabase/GitHub'a göndermez. OAuth geliştirici bağlantısı yapılandırılmadı. Google/Apple tarayıcı oturumu uygulamaya aktarılmaz. Gömülü tarayıcı veya DRM sınırları aşılmaz. Girişsiz gerçek web görünümü test edildi; giriş sonrası tam çalma doğrulanmadı.
## 4.4 oturum, arama, ses ve GIF

Kalıcı oturum Windows CurrentUser DPAPI ile korunur; parola saklanmaz. Atomik dosya değişimi uygulanır. Çevrimdışı açılış korunan kimliği silmez; istekler sunucuda doğrulanmaya devam eder. Reddedilmiş/iptal edilmiş yenileme oturumu temizler. Devam eden yenileme çıkışı geri alamaz. Fixture HTTP testleri hatırla/hatırlama, yeniden açma, çevrimdışı tekrar bağlanma, token yenileme ve iptal kontrollerinden geçti.

Keşfet yalnızca herkese açık veya çağıranın üyesi olduğu sunucuları döndürür. Diğer özel sunucular görünmez. Arama üyelik oluşturmaz. Türkçe ad, boşluklar, kategori, görünürlük açma/kapatma, özel sunucu ve yasaklı erişim transaction/rollback testlerinden geçti; test kullanıcıları kalmadı.

Ses tablolarında RLS açıktır; doğrudan istemci erişimi ve anonim RPC kapalıdır. auth.uid(), oda türü, üyelik, yasak, aktif oturum kimliği, gönderen/alıcı ve engelleme kontrolleri sunucudadır. Kanal altı katılımcı ve tek paylaşım ile sınırlıdır. Sinyaller 65 kB ve çağrılar kullanıcı başına dakikada 420 ile sınırlıdır. 30 saniye yenilenmeyen oturumlar ve 60 saniyeden eski sinyaller bir sonraki RPC sırasında temizlenir; ayrı zamanlanmış silme işi kurulmadı. Hesap değişimi, çıkış ve bilinen yetki/oturum reddi yerel medya izlerini durdurur.

Ses/görüntü WebRTC DTLS/SRTP aktarımıdır. Medya Pakla veritabanından geçmez; SDP/ICE sinyalleri Supabase'de kısa süreli bulunur. Google STUN kullanılır; katılımcılar/STUN hizmeti bağlantı IP bilgilerini görebilir. TURN/SFU yoktur; belirli NAT ve kurumsal ağlarda bağlantı başarısız olabilir. Bu bir Discord ölçeğinde ses altyapısı veya özel mesajlar için uçtan uca şifreleme iddiası değildir. İki gerçek WebView2 istemcisinde sentetik ses/video doğrulandı; gerçek kullanıcılar arası farklı ağ/mikrofon/ekran seçicisi testi yapılmadı.

Ses WebView yalnızca gömülü pakla.local sayfasını açar. Host objects, dış sayfalar, indirmeler, otomatik parola kaydı ve geliştirici araçları kapalıdır. Mikrofon varsayılan kapalıdır ve izin ister; ekran kaynağı kullanıcı seçicisinden alınır. Kamera kullanılmaz. Kaynaklar kapanışta bırakılır. Pakla erişim tokenı WebView içeriğine verilmez. Spotify ve ses görünümü ortak WebView2 yükleyicisini kullanır.

KLIPY istemci uygulama anahtarı sadece GIF kataloğu içindir; hesap/yönetim anahtarı değildir. Test kotası uygulama için ortak 100 API çağrısı/saattir; üretim onayı henüz yoktur. İstekler doğrudan resmi Klipy API'sine gider; anonimleştirilmiş sabit müşteri kimliği ve arama terimi iletilir. E-posta, parola, Supabase tokenı ve sohbet metni gönderilmez. Medya URL'leri API'nin verdiği biçimde korunur; izinli resmi HTTPS medya alan adlarından doğrudan, geçici belleğe yüklenir. Diskte medya cache/proxy yoktur. Alıcı uzak GIF'i tıklamadan yükleme yapılmaz. Boyut, GIF başlığı, piksel/frame sınırları ve yönlendirme yasağı uygulanır. Başarısız izleme isteği mesaj gönderimini bekletmez. Reklamlar etkinleştirilmedi. Search KLIPY / Powered by KLIPY atfı görünür.

Lucide ISC lisansı dağıtım dosyasında ve uygulamaya gömülü lisans ekranında bulunur. Pakla, Discord veya Medal'ın resmi ürünü değildir. Oyun enjeksiyonu, anti-cheat müdahalesi veya antivirüs atlatma özelliği eklenmedi.
## 4.5 görünüm değişikliği

Sunucu/sohbet düzeni, kompakt mesaj çubuğu ve kullanıcı alt şeridi yenilendi. Sunucu son kanal hafızası ve arkadaş filtresi yalnızca yerel oturumdadır, hesap değişiminde temizlenir. Alt mikrofon/kulaklık düğmeleri aktif ses oturumu dışında kapalıdır; açıkken güvenilir yerel WebView'e komut iletir ve mevcut izin akışını kullanır. Kontrollerin kapalı/etkin durumu ve komut yönlendirmesi test verileriyle doğrulandı. Yeni servis, yönetici yetkisi veya bulut izin değişikliği yoktur. 4.5 yerel denemesinin görünümü 4.6 genel güncellemesine dahil edildi. Güncelleme kullanıcı onayıyla kurulur.