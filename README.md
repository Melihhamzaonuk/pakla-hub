# Pakla Hub 4.10.2

Sohbet, topluluklar, klipler ve bilgisayar araçları aynı uygulamada.

[Windows x64 için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar **Ayarlar → Güncellemeler → Güncelleme ara** ile 4.10.2 paketini yükleyebilir. Kütüphane ve hesap verileri korunur. Bildirimler açıksa açılışta ve uygulama açıkken altı saatte bir sürüm kontrol edilir. Kurulum kullanıcı onayıyla yapılır.

## Açılışta güncelleme bildirimi

Güncelleme bildirimi tercihi açıkken Pakla, açılıştan kısa süre sonra resmi kanalı kontrol eder. Yeni sürüm bulunursa **Güncelleme hazır** penceresinde yenilikler görünür. **Güncellemeyi incele** uygulama içindeki güncelleme ekranını açar; **Daha sonra** aynı sürümün o oturumdaki tekrarını durdurur. Uygulama gizliyken pencere gösterilmez; geri açıldığında bekleyen bildirim görünür. Kurulum kendiliğinden başlamaz. Kontrol için internet gerekir; bağlantı hatası açılışı engellemez.

## Açılış düzeltmesi

4.10.2, ana sayfanın pencere hazır olmadan arka plan yenilemesi başlatmasından kaynaklanan açılış çökmesini giderir. Arka plan açık gerçek pencere başlangıcı üç kez sınandı. Önceki sürüm açılmıyorsa yukarıdaki güncel kurulumu indirip çalıştırabilirsin; uygulamayı kaldırman gerekmez.

## Yeni hızlı geçiş

**Ctrl+K** artık yüklenmiş arkadaş, sunucu ve kanal listelerinde de arar. `@isim` arkadaşları, `#kanal` kanalları süzer. Türkçe karakterler ve birden fazla arama sözcüğü desteklenir. Listeleri yenile düğmesi güncel verileri yeniden ister. Sonuç seçmek sohbeti veya kanalı açar; ses kanalına otomatik katılım yapılmaz.

## Paylaşılan bağlantılar ve GIF'ler

Sohbet veya kanal başlığındaki bağlantı simgesini aç. Dar kanallarda **Diğer kanal işlemleri** menüsündedir. Yalnızca o konuşmada yüklenmiş mesajlar taranır; eski içerik için önce mesaj geçmişini yükle.

Bağlantılar alan adı ve tam adresiyle listelenir. Tekrarlanan adresler birleştirilir. Tam adresi inceleyip varsayılan tarayıcıda açmayı seçebilir veya mesajı alıntılayabilirsin. HTTP/HTTPS desteklenir; kimlik bilgisi taşıyan ve desteklenmeyen protokollü adresler listeye alınmaz. Bağlantılar kendiliğinden açılmaz. Uzak GIF'ler göster düğmesine basınca Klipy'den yüklenir.

![Paylaşılan bağlantılar — örnek adresler ve test mesajları](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.10.2/Pakla-Paylasilanlar.png)

## Çoklu klip düzenleme

Klipler ekranında **Çoklu seç** düğmesine bas. Kartı veya seçim kutusunu kullan; **Bu sayfayı seç** ile sayfanın tamamını seçebilirsin. Seçim, sayfalar arasında korunur; filtre değişiminde temizlenir. Başka ekrana veya hesaba geçince seçim modu kapanır.

Seçilen klipleri topluca favorilere ekle/çıkar veya bir koleksiyona ata. Boş koleksiyon adı atamayı kaldırır. Bu işlemler yalnızca metadatayı değiştirir; videolar taşınmaz veya yeniden kodlanmaz. Kaydetme başarısız olursa önceki değerler geri yüklenir.

![Çoklu seçim — yerel test kapakları](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.10.2/Pakla-TopluKlipler.png)

Önizlemelerdeki kişiler, klipler ve kapaklar test verileridir; kullanıcıya eklenmez. Gelen kutusu, sabit sohbetler, profil sekmeleri, geri/ileri ve Pakla araçları korunur.

## Mevcut sınırlar

Ses/ekran beta: 6 kişi, tek paylaşım; TURN/SFU yok, bazı ağlar bağlanamayabilir. Farklı ağlarda gerçek mikrofon ve ekran seçimi testi tamamlanmadı. KLIPY ortak test kotası saatte 100 API isteğidir. Spotify OAuth yapılandırılmadı; giriş sonrası tam oynatma doğrulanmadı. Mesajlarda uçtan uca şifreleme yoktur. Klipler kendiliğinden buluta yüklenmez. Internet Booster bağlantı ölçümü yapar; VPN değildir. Oyun belleğine ve anti-cheat sistemlerine müdahale edilmez.

Windows 10/11 x64, .NET Framework 4.8 ve ses/Spotify için Edge WebView2 Runtime gerekir. Patch RSA-SHA256 ile doğrulanır. Windows Authenticode yayıncı sertifikası henüz yoktur. Son dosyaların Kaspersky taramasında 36 nesne, 0 tespit, 0 şüphe ve 0 hata görüldü; tüm güvenlik ürünleri için garanti değildir.

Kontroller: QUALITY-REPORT.md, release-verification.json, SHA256SUMS.txt, antivirus-report.txt ve SECURITY.md. Üçüncü taraf lisansları uygulamada ve THIRD-PARTY-LICENSES.txt dosyasındadır.

Destek: supportpakla@gmail.com