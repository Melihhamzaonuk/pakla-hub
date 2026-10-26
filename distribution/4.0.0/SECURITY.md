# Pakla Hub 4.0 güvenlik notları

4.0.0 son dosyaları Kaspersky 21.26 ile tarandı: 4 nesne, 0 tespit, 0 şüphe, 0 hata. Son dosyaların SHA-256 değerleri release-verification.json, yerel tarama sonucu antivirus-report.txt içindedir. Sonuç bu dosyalar ve tarama anı içindir; tüm güvenlik ürünleri için garanti değildir.

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
