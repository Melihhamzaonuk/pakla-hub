# Pakla Hub 3.1 güvenlik notları

3.1.1 uygulama, kurulum, güncelleyici ve imzalı patch dosyalarının yerel Kaspersky 21.26 taramasında 19 nesne kontrol edildi: 0 tespit, 0 şüphe, 0 hata. SHA-256 değerleri release-verification.json, tarama sonucu antivirus-report.txt içindedir. Sonuç bu dosyalar ve tarama anı içindir; tüm güvenlik ürünleri için garanti değildir.

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
