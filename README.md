# Pakla Hub · 4.3

Sohbetlerin, sunucuların, kliplerin ve araçların. Tek bir yerde.

**[Pakla Hub’ı indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)**

Kurulu uygulamada **Ayarlar → Güncellemeler → Güncelleme ara → Patch yükle**. 2.1 ve üzeri sürümler imzalı patch alabilir; yerel veriler korunur.

## Yenilenen kayıt ve simgeler

Monitör kaydı DXGI Desktop Duplication kullanır: Windows Graphics Capture'ın sarı monitör çerçevesi açılmaz. Kayıt elle başlar; uygulama ve tepsi kayıt durumunu göstermeyi sürdürür. Yeni klip durum kartı, animasyonlu karşılama alanı, gömülü Pakla simgesi ve sürümlü kısayol simgeleri eklendi. Windows simge önbelleği silinmez, Explorer yeniden başlatılmaz.

## Kendi sunucunu kur

Oyun ekibi, içerik topluluğu, çalışma grubu veya boş başlangıç şablonuyla başla. Sunucular varsayılan davetlidir. Sunucu adına veya **Sunucu ayarları** düğmesine tıklayarak düzenle:

- Ad, açıklama, kurallar, ikon ve banner.
- Kategoriler, kategori daraltma, kanal sırası ve konusu.
- Herkesin yazabildiği metin ve yalnızca yöneticilerin yazabildiği duyuru kanalları.
- Kanal arşivleme ve arşivden geri açma; mesajlar korunur.
- Renkli özel roller; kurucu arkadaşına yönetim yetkili rol atayabilir. Bir üyede bir özel rol bulunur.

Yönetim yetkisi görünüm, kategori/kanal, davet ve üye/mesaj moderasyonunu kapsar. Rol/yetki dağıtımı, Keşfet görünürlüğü ve sunucu arşivleme kurucudadır.

**Keşfet** yalnızca kurucunun listelemeyi açtığı gerçek sunucuları kategori ve ad/açıklama aramasıyla gösterir. Önizlemede tanıtım ve kurallar görünür; mesajlar üyelikten önce açılmaz. Değişmiş kurallar katılımda yeniden incelenir. Sahte sunucular/çevrimiçi sayıları gösterilmez.

Kullanıcı başına 20 aktif sunucu, 5 kuruculuk; sunucu başına 100 üye, 20 aktif kanal, 12 kategori, 12 özel rol. Davetler 7 gün/25 katılım; Keşfet sayfaları en fazla 24 sonuç. Sesli/görüntülü kanallar, ekran paylaşımı ve Discord'un ayrıntılı kanal izin matrisi henüz yoktur.

## Sohbet, profil ve klipler

Doğrulanmış Pakla hesabıyla arkadaş ekle, birebir mesajlaş, avatar ve bannerını canlı önizlemeyle düzenle. Topluluk kanallarında altı emoji tepkisi, kendi mesajını düzenleme, alıntı metni, yönetici sabitleri ve Ctrl+F araması bulunur. Kanal başına 50 görünür sabit; aramada son 10.000 aday mesajdan en fazla 60 sonuç.

Mesajlar sunucuda saklanır; **uçtan uca şifreli değildir**. E-postalar sosyal profilde gösterilmez. Yeniden deneme mesajı çoğaltmaz. Taslaklar bellektedir, hesap değişiminde temizlenir. Aktif kanal yaklaşık 3, özel sohbet 2,5 saniyede yenilenir.

720p30/1080p30/1080p60 klip kaydı; varsayılan 1080p30 ve mikrofon kapalıdır. Ctrl+Shift+F8 son yaklaşık 15/30/60 saniyeyi saklar. Tampon 256 MB; en az 1 GB boş alan gerekir. 10 saniyelik parçalar arasında kısa kesintiler olabilir. Klipler yereldir, otomatik paylaşılmaz. Windows korumalı içerik kaydını sınırlandırabilir; hedef FPS yük altında garanti edilmez.

## Spotify ve yerel müzik

Yerel MP3/WAV oynatıcısı korunur. **Kitaplık → Spotify** veya **Müzik → Spotify uygulama içinde aç** resmi Spotify web görünümünü açar. Parça, albüm, liste ve podcast bağlantıları resmi gömülü oynatıcıda açılabilir. Microsoft Edge WebView2 Runtime gerekir. Tam oynatma hesap, bölge ve gömülü tarayıcı desteğine bağlıdır.

Google/Apple girişi gömülü oynatıcıda desteklenmez. **Tarayıcıda giriş** normal tarayıcıyı açar; o oturum Pakla'ya otomatik aktarılmaz. İçeride Spotify e-posta girişini kullanıcı kendisi yapar. Spotify geliştirici/OAuth bağlantısı henüz yapılandırılmamıştır; giriş sonrası tam çalma doğrulanmadı. Pakla Spotify parolası veya erişim tokenı almaz. Yerel web oturumu ayrı profildedir; Pakla hesabı değişince oynatıcı kapanır. Oturum temizleme düğmesi yalnızca bu yerel web oturumunu siler.

## Araçlar ve güvenlik

Clean, bağlantı ölçümü, sistem göstergeleri, büyük dosyalar, başlangıç kayıtları, oyun/uygulama kısayolları, raporlar ve patch merkezi korunur. Internet Booster gecikme, jitter ve yanıt kaybını ölçer; VPN/GearUP benzeri yönlendirme yapmaz. Oyun belleğine veya anti-cheat sistemlerine müdahale edilmez.

Windows 10/11 x64, .NET Framework 4.8, kayıt için Media Foundation ve Visual C++ x64 çalışma zamanı gerekir. X varsayılan tepsiye küçültür; tamamen çıkış tepsi menüsündedir. Kayıt/müzik açılışta başlamaz. Animasyonlar kapatılabilir. Discord aktivitesi isteğe bağlı ve varsayılan kapalıdır; yalnızca genel Pakla durumu paylaşılır.

RSA-SHA256 patch doğrulaması vardır; bu derleme güvenilir Windows Authenticode yayıncı sertifikası taşımaz. [Güvenlik](distribution/4.3.0/SECURITY.md), [doğrulama](distribution/4.3.0/release-verification.json), [tarama](distribution/4.3.0/antivirus-report.txt), [lisanslar](distribution/4.3.0/THIRD-PARTY-LICENSES.txt).

Hesaplar Supabase, doğrulama e-postaları Brevo kullanır. Pakla oturumları Windows DPAPI ile korunur; SMTP/yönetici anahtarları dağıtılmaz.

Destek: **supportpakla@gmail.com**
