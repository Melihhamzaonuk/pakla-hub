# Pakla Hub · 2.4 Compact

Windows için kompakt neon oyun ve bakım merkezi.

**[İlk kurulum için Pakla Hub'ı indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)**

**2.1, 2.2 veya 2.3 kuruluysa:** Güncellemeler → Güncelleme ara → Patch'i yükle.

## 2.4 ile gelenler

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
