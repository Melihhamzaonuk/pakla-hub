# Pakla Hub · 2.2 Feature Drop

Windows için neon tasarımlı uygulama ve bakım merkezi.

**[Pakla Hub kurulumunu indir](https://raw.githubusercontent.com/Melihhamzaonuk/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)**

**2.1 kuruluysa:** Güncellemeler → Güncelleme ara → Patch'i yükle. Yeniden kurulum dosyası indirmek gerekmez.

## 2.2 ile gelenler

- **Live Dashboard:** CPU/RAM ve indirme/yükleme trafiğinin son 120 örneğini canlı grafiklerde izle; disk doluluğunu gör.
- **Büyük Dosyalar:** Seçilen klasörde en büyük 500 dosyayı bul. Desteklenen belge, medya ve arşivleri onayınla Geri Dönüşüm Kutusu'na taşı.
- **Başlangıç:** Run kayıtlarını ve Başlangıç klasörlerini incele; etkinleştirme/devre dışı bırakma için Windows'un kendi başlangıç ekranını aç.
- **Bağlantı Geçmişi:** Son 500 ölçümü yerelde sakla, isteğe bağlı 30 saniye aralıklı izlemeyi başlat ve CSV olarak kaydet.
- **Neon Studio:** Cyan, mor, kırmızı veya özel vurgu rengi; kompakt menü ve listeler. Tercihler saklanır.
- **Güncelleme bildirimi:** Uygulama açıkken açılışta ve 6 saatte bir yeni sürümü kontrol eder. Paket yüklemek için kullanıcı onayı gerekir; kapatılabilir.

## Diğer araçlar

Pakla Clean, Internet Booster, uygulama kütüphanesi, imzalı Patch Center ve Ayarlar üzerinden kaldırma.

## Bilmen gerekenler

- Windows ve .NET Framework 4.7+ gerekir. Kurulum exe'si Authenticode imzalı değildir; patch'ler RSA-SHA256 ile ayrıca doğrulanır.
- Büyük dosya taraması seçtiğin klasörle sınırlıdır. Sistem, program ve bilinen oyun klasörleri atlanır; bağlantılı dosya/klasörler izlenmez. 250.000 öğe sınırında kısmi sonuç gösterilir.
- Kutudaki dosyalar alan kullanmaya devam eder. Windows kalıcı silme önerirse işlemi iptal et.
- Başlangıç listesi tüm otomatik başlatma yöntemlerini kapsamaz ve Windows'ta kapatılmış kayıtları da içerebilir. Yönetim Windows'a bırakılır.
- Bağlantı ölçümleri sadece sen başlatınca yapılır; ICMP engeli yanıtsızlığa neden olabilir. Anlık trafik bir hız testi değildir.
- Telemetri gönderilmez. Kütüphane, tercihler ve bağlantı geçmişi bu bilgisayarda saklanır; kaldırmada korunur.
- Sistem izleme salt okunurdur. Oyun işlemi önceliği değiştirme, bellek müdahalesi, DLL veya overlay özelliği yoktur. FPS artışı veya ban olmayacağı garantisi verilmez.
- 2.0 ve daha eski sürümler bir defalık yeni kurulum gerektirir.

Bu depo resmi kurulum ve güncelleme dosyalarının dağıtımı içindir.
