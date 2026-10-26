# Pakla Hub · 3.3

Windows için oyun, klip ve bakım merkezi.

**[Pakla Hub’ı indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)**

2.1 ve üzeri kuruluysa Güncellemeler → Güncelleme ara → Patch yükle.

## Yeni görünüm ve netlik

Yüksek DPI ve monitör ölçeği desteği, ölçeklenen vektör ikonlar, daha okunaklı yazılar, sade yüzeyler, ortak arama çubuğu ve yenilenen giriş alanları. Dar pencerede menü ve kartlar uyarlanır; hareketler ayarlardan kapatılabilir.

1080p60 daha fazla GPU, disk ve güç kullanır. Kaynak ekranın çözünürlüğü veya kare hızı daha düşükse yükseltmek yeni görüntü ayrıntısı oluşturmaz. Sabit FPS hedefi, yük altında gerçek yakalama hızını garanti etmez.

## Arkadaşlar ve özel sohbet

Arkadaşlar bölümünde kendi arkadaş profilini etkinleştir ve benzersiz kullanıcı adını seç. Diğer kullanıcılar seni bu adla bulur; e-posta adresin aramada paylaşılmaz. Arkadaşın da kendi profilini etkinleştirmelidir.

- Kullanıcı adıyla arama; gelen/giden istekler, kabul, ret ve iptal.
- Kabul edilen arkadaşlar arasında birebir metin sohbeti.
- Okunmamış mesaj sayısı, gönderildi/okundu bilgisi ve önceki mesajları yükleme.
- Enter ile gönder; Shift+Enter ile yeni satır. Mesaj sınırı 2000 karakter.
- Bağlantı hatasında taslak korunur; tekrar gönderim aynı mesajı çoğaltmaz.
- Arkadaşlıktan çıkarma, engelleme ve engeli kaldırma. Engel kalkınca yeni arkadaş isteği gerekir.

Mesajlar uygulama açıkken yaklaşık 2,5 saniyelik aralıklarla alınır. Arkadaş/okunmamış listesi sosyal ekranlarda yaklaşık 5, arka planda 30 saniyede yenilenir. Çevrimiçi durum veya yazıyor bilgisi gösterilmez. Grup, sesli görüşme ve dosya eki bu sürümde yoktur.

Mesajlar Supabase sunucusunda saklanır; uçtan uca şifreli değildir. Veritabanı erişim kuralları yalnızca katılımcı kullanıcı hesaplarına okuma izni verir. Üçüncü kullanıcı, misafir ve doğrudan yazma denemeleri reddedilir. Sunucu mesaj uzunluğunu, arkadaşlık/engel durumunu ve gönderim hızını doğrular. Mesaj metinleri düz metin olarak gösterilir; HTML çalıştırılmaz.

Gönderilmemiş taslaklar uygulama açıkken bellekte korunur; çıkış yapıldığında temizlenir. Mesaj geçmişi ve arkadaş listesi hesaba bağlı olarak sunucudan alınır.
## Tek bir ana alan

- Sabit ortak çubuk: oyun, klip ve uygulama araması; kayıt durumu, etkinlikler ve profil.
- Kendi masan: sık kullandığın araçları ana alana sabitle.
- Son kliplerin, oyun kısayolların, canlı CPU/RAM/disk bilgileri ve bakım araçların aynı yerde.
- Neon yüzeyler, hareketli görseller, hover geçişleri ve dar pencereye uyarlanan menü. Animasyonlar kapatılabilir.

## Klip stüdyosu ve profil

- Seçtiğin monitörü 720p30, 1080p30 veya 1080p60 MP4 olarak kaydet. Varsayılan 1080p30. Kayıt elle başlatılır.
- Ctrl+Shift+F8 ile son yaklaşık 15, 30 veya 60 saniyeyi sakla.
- Yerel klip kütüphanesi: arama, favoriler, sıralama, ad düzenleme ve MP4 kopyası dışa aktarma.
- Sistem tepsisinde çalışma, durdurma, kaydetme ve tamamen çıkış.
- E-posta doğrulamalı kayıt/giriş, şifre sıfırlama, profil görseli, biyografi ve kapak rengi.
- Profilde bu cihazdaki öne çıkan kliplerin. Klipler otomatik paylaşılmaz veya buluta yüklenmez.

## Pakla araçların

Pakla Clean, Internet Booster, canlı sistem göstergeleri, bağlantı geçmişi, büyük dosya bulucu, başlangıç kayıtları, oyun ve uygulama kütüphanesi, temizlik raporları ve uygulama içi imzalı güncellemeler.

## Kullanım bilgileri

Windows x64 ve .NET Framework 4.8+ gerekir. Kaydedilen ekran masaüstünü ve bildirimleri de içerebilir. Mikrofon varsayılan olarak kapalıdır. Tampon 10 saniyelik parçalardan oluşur; parçalar arasında kısa kesintiler olabilir. Yaklaşık klip süresi eldeki görüntüye bağlıdır; tampon en fazla 256 MB tutulur. Kayıt için en az 1 GB boş alan gerekir.

Oyunlar yalnızca kendin eklediğin güvenilir kısayollarla başlatılır. Oyun belleğine veya anti-cheat'e müdahale edilmez. Seans sayacı Hub açıkken geçen süreyi ölçer. Internet Booster gerçek ping/jitter ölçümleri sunar; FPS veya internet hızı artışı garantisi vermez.

Temizlik ekranındaki kalıcı silme için dosya listesini inceleyip onay ver. Desteklenen büyük dosya ve klip kaldırmaları Geri Dönüşüm Kutusu'nu kullanır. Güncellemeler ve kaldırma kişisel verileri korur.

Hesap ve profil için Supabase, doğrulama e-postaları için Brevo kullanılır. “Beni hatırla” oturum anahtarlarını Windows DPAPI ile korur; şifre yerelde saklanmaz. SMTP ve yönetici anahtarları uygulamaya dahil edilmez. Klipler, oyun kısayolları ve ölçümler cihazında tutulur.

## Yayın güvenliği

Patch paketleri RSA-SHA256 imzası ve dosya özetleriyle doğrulanır. Windows Authenticode yayıncı sertifikası henüz yoktur. Yerel antivirüs taraması ve dosya özetleri: [güvenlik notları](distribution/3.3.0/SECURITY.md), [doğrulama kaydı](distribution/3.3.0/release-verification.json), [tarama raporu](distribution/3.3.0/antivirus-report.txt). Sonuçlar yalnızca ilgili dosyalar ve tarama anı içindir.

ScreenRecorderLib 7.0.1 MIT lisansıyla kullanılır; lisans uygulamanın kayıt çalışma zamanı klasörüne çıkarılır.

Destek: **supportpakla@gmail.com**