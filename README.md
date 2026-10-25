# Pakla Hub · 2.5 Visual

Windows için kompakt neon oyun ve bakım merkezi.

**[İlk kurulum için Pakla Hub'ı indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)**

**2.1–2.4 kuruluysa:** Güncellemeler → Güncelleme ara → Patch'i yükle.

## 2.5 ile gelenler

- **Esnek görsel düzen:** Dar pencerede ikon menüsü ve tek sütun; geniş pencerede çok sütun. Araç kartları, canlı halka göstergeleri, hareketli kontrolcü sahnesi ve 160 ms hover geçişleri. Hareketler ayarlardan kapatılabilir.
- **Kompakt ana ekran:** Beş ana menü, tek bakışta CPU/RAM/disk özeti, son başlatılanlar ve hızlı işlemler.
- **Ctrl+K:** Araçlarını ve oyunlarını yazıp bul; ok tuşları ve Enter ile aç.
- **Otomasyon:** Uygulama açıkken açılışta ve saatte bir, 7 günden eski yerel geçici dosyaların salt okunur taraması. Dosya silmez; 15 saniye sınırı vardır. Ayarlardan kapatılabilir.
- **Seans araçları:** Rastgele oyun önerisi, son başlatılanlar ve isteğe bağlı oyun başlatınca küçülme. Seans sayacı yalnızca bu Hub oturumunda geçen süreyi ölçer; gerçek oyun süresi değildir.
- **Neon açılış:** Bir saniyeden kısa ve atlanabilir animasyon. Ayarlar → Otomasyon bölümünden kapatılabilir.
- **Game Shelf:** Kendi Windows `.lnk` veya sade Steam `.url` kısayollarını ekle. Kapak görseli, favori, arama ve sayfalama desteği.
- **Temizlik raporları:** Bu sürümden itibaren tamamlanan/durdurulan temizliklerin dosya sayısını, silinen dosya boyutlarını ve atlananları gör; CSV kaydet.
- **Bağlantı karşılaştırması:** Aynı hedef IP'nin saatlik/günlük özetlerini karşılaştır. Ping ortalaması alınan yanıt sayısıyla ağırlıklandırılır. Sınırlı özetler en fazla 60 gün saklanır.
- **Ölçümlere dayalı öneriler:** Disk alanı, yeterli sayıda CPU/RAM örneği ve yanıtsız ping paketleri için eşik tabanlı öneriler. Değişiklik otomatik yapılmaz.
- **Sürüm geçmişi:** Yerel kurulum/patch kayıtları ve sürüm notları. Önceki kayıtlar yalnızca mevcut güncelleme makbuzları/yedekleri varsa aktarılabilir.

Temizlik raporları, öneriler, başlangıç kayıtları, büyük dosyalar ve sürüm geçmişi **Araçlar** bölümündedir.

## Önceki araçlar

Canlı CPU/RAM/ağ grafikleri, büyük dosya bulucu, Windows başlangıç yönetimine geçiş, bağlantı geçmişi/izleme/CSV, neon temalar, kompakt görünüm, güncelleme bildirimi, uygulama kütüphanesi ve kaldırma.

## Bilmen gerekenler

- Windows ve .NET Framework 4.7+ gerekir. Kurulum exe'si Authenticode imzalı değildir; patch'ler RSA-SHA256 ile ayrıca doğrulanır.
- Oyunlar otomatik taranmaz; yalnızca güvendiğin kısayolları kendin ekle. Kapaklar yerel PNG/JPG dosyalarından seçilir. Doğrudan oyun exe'si, ek başlatma parametresi, DLL, overlay veya işlem önceliği ayarı eklenmez.
- Telemetri gönderilmez. Kütüphane, kapaklar, düzen, raporlar ve ölçümler bu bilgisayarda kalır; kaldırmada korunur.
- Temizlik kalıcı siler. Büyük dosya aracının desteklenen kutuya taşıma işlemi ayrıdır; dosya listesini ve onayları incele.
- Silinen dosya boyutu fiziksel boşalan disk alanıyla aynı olmayabilir.
- Karşılaştırmalar yalnızca gerçekten alınmış ölçümleri kapsar; uygulama kapalıyken ölçüm yapılmaz. ICMP yanıt kaybı, internet kesintisi kanıtı değildir.
- Oyunlara veya anti-cheat'e müdahale eden booster özelliği yoktur. FPS artışı veya ban olmayacağı garantisi sunulmaz.
- 2.0 ve daha eski sürümler bir defalık yeni kurulum gerektirir.

Bu depo resmi kurulum ve imzalı güncelleme paketlerinin dağıtımı içindir.

## Yayın güvenliği

2.5.0 yayın dosyalarının yerel Kaspersky 21.26 taramasında 11 nesne incelendi; 0 tespit, 0 şüphe ve 0 hata raporlandı. Sonuç belirtilen dosya özetleri ve tarama anı içindir; bütün ürünler için garanti değildir. Bu derleme Authenticode imzalı değildir. Ayrıntılar: [güvenlik notu](distribution/2.5.0/SECURITY.md), [dosya doğrulaması](distribution/2.5.0/release-verification.json), [tarama raporu](distribution/2.5.0/antivirus-report.txt).
