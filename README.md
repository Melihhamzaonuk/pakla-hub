# Pakla Hub 4.15

Ekibin, anların ve araçların. Windows x64 masaüstü uygulaması.

[Windows için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar Ayarlar → Güncellemeler → Güncelleme ara ile 4.15.0 paketini yükleyebilir. Güncelleme bildirimleri açıksa yeni sürüm açılışta duyurulur; kurulum kullanıcı seçimiyle başlar.

## Bu sürümde

- Açılışta simge yenileme ve açılır menü kapanışı sırasında saptanan iki çökme nedeni düzeltildi.
- Topluluklara banner/ikonlu başlık, kanal araması ve kolay metin, duyuru, ses kanalı oluşturma eklendi.
- Kanal izinlerinde herkes ve özel roller için görme, mesaj gönderme, bağlanma, konuşma, kamera ve ekran paylaşma ayrı düzenlenebilir. Kurucu ve yöneticiler erişimini korur.
- DM’den sesli ve görüntülü arama davetleri gönderilebilir. Karşı taraf kabul eder veya reddeder; mikrofon ve kamera kullanıcı açana kadar kapalıdır. İki taraf da 4.15 kullanmalıdır.
- DM, grup, topluluk ve kanal bildirimleri süreli veya süresiz susturulabilir. Tercihler bu cihazda hesap bazında saklanır.
- İnternet aracı otomatik bağlantı/DNS tanısı ve kullanıcı seçimiyle onarım sunar. Özel arkadaş grupları, kamera ve ekranı birlikte paylaşma, cihaz seçimi ve katılımcı ses ayarı bulunur.

Sohbet, GIF’ler, yerel klip kütüphanesi, koleksiyonlar, hızlı arama, şifreli yerel taslaklar ve bilgisayar araçları korunur. Temizlik seçerek yapılır; FPS veya internet hızı artışı garanti edilmez.

## Geliştirme durumu

Ses, görüntü ve ekran paylaşımı beta: en fazla altı kişi, aynı anda bir ekran paylaşımı. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. İki istemcili sentetik medya ve yeniden bağlantı testleri geçti; altı kişilik yük ve gerçek kişisel kamera/mikrofon testleri tamamlanmadı. Kanal erişimi ve ses sinyalleri sunucuda denetlenir; doğrudan P2P medya için değiştirilmiş istemcileri filtreleyen bir SFU bulunmaz.

KLIPY ortak test kotası 100 API çağrısı/saat. Spotify OAuth yapılandırılmadı. Mesajlar uçtan uca şifreli değil. Windows yayıncı sertifikası bulunmuyor; patch paketleri ayrı RSA-SHA256 imzasıyla doğrulanır.

Destek: supportpakla@gmail.com
