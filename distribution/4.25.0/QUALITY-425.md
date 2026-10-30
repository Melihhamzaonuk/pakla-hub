# Pakla Hub 4.25.0

Modern kurulum ekranı, EXE içine gömülü 16 saniyelik sessiz/döngülü tanıtım ve başarılı kurulumdan sonra otomatik kapanma. Uygulama açılışı başarısız olursa kurulum yeniden yapılmadan tekrar denenebilir.

X düğmesi tek tıklamayla güvenli çıkış ister: devam eden mesaj/klip işleri tamamlanır, iptal edilebilen indirme ve taramalar durdurulur, kayıt tamponu kapatılır. İkinci tıklama gerekmez. Kapatma beklerken pencerenin tepsi/uyandırma sinyaliyle geri açılması engellenir. Arka planda tutmak için ayrı Tepsiye küçült düğmesi vardır.

4.24 geliştirmeleri de dahildir: koyu/sarı klip kütüphanesi, arama, favoriler, koleksiyonlar, sıralama ve çoklu seçim; süre cetvelli klip kırpma; manuel Game Boost odak oturumu; Windows VPN profil yönetimi; DM/topluluk yazma alanı iyileştirmeleri.

## Doğrulama

- Uygulama ve kurulum self-testleri geçti.
- Kurulumda otomatik kapanma, yalnızca bir kez başlatma, başlatmadan kapanma, çift tıklama koruması, yükleme hatasında yeniden deneme ve açılış hatasında yeniden kurmadan deneme geçti.
- Devam eden iş sonrasında tek kapatma isteğiyle çıkış ve bekleyen kapatma sırasında geri açılmama testi geçti.
- Gerçek WebView2 oynatıcısında gömülü 1280x720 H.264 tanıtımın çözümlenmesi, zamanın ilerlemesi, sessiz oynatma ve döngü ayarı doğrulandı. WebView2 yoksa tanıtım posteri gösterilir; kurulum engellenmez.
- Klip arama/sıralama/seçim komutları, dar görünüm ve metin enjeksiyonu koruması test edildi. Zaman çizgisi sınırları ve ondalıklı süreler test edildi.
- RSA imzası, dosya hashleri, bozuk imza/içerik, yol aşımı ve sürüm düşürme reddi, uygulama/geri alma ve veri koruma testleri geçti. Gerçek 4.23 uygulamasının güncelleme test hattı 4.25 paketini doğrulayıp izole klasöre uyguladı.

## Sınırlar

Tanıtım ve ekran görüntülerindeki klip/mesaj içerikleri gösterim verisidir. Gerçek iki hesapla mesajlaşma, canlı oyun kaydı ve gerçek VPN bağlantısı bu sürüm çalışmasında uçtan uca denenmedi. VPN hizmeti/sunucusu verilmez; mevcut Windows profilleri yönetilir. Game Boost Pakla'nın arka plan yükünü azaltır; FPS garantisi içermez.

Windows Authenticode yayıncı sertifikası yapılandırılmadı. Otomatik güncelleme paketinin RSA imzası ayrı mekanizmadır ve önceki güven anahtarıyla doğrulanır. Kaynak kodları herkese açık değildir.
