# Pakla Hub 4.18

Ekibin, anların ve araçların. Windows x64 masaüstü uygulaması.

[Windows için indir](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/PaklaHub-Kurulum.exe)

Mevcut kullanıcılar **Ayarlar → Güncellemeler → Güncelleme ara** yolundan 4.18.0'a geçebilir. Güncelleme bildirimleri açıksa yeni sürüm açılış kontrolünde duyurulur; yükleme kullanıcı seçimiyle başlar.

## Daha düzenli bir çalışma alanı

Geniş ekranda sabit sol gezinme, sohbetlerde kompakt simgeler, dar pencerede bölüm menüsü. Ana sayfadan arkadaş sohbetlerine, kliplere ve araçlara geç. Üstte geri/ileri ve Ctrl+K arama; Ctrl+1–6 ile ana bölümlere ulaş.

![Yeni ana ekran — örnek test verileri](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.18.0/Pakla-AnaSayfa.png)

## Ekibinle aynı yerde

Sohbet ve kanallarda iki satırlı başlık, görünür GIF düğmesi, Enter/Shift+Enter açıklaması; koyu menüler ve ortalanmış komut simgeleri. Yüksek DPI'da kalıtılan yazının ikinci kez büyütülmesi düzeltildi.

![Topluluk görünümü — örnek test verileri](https://raw.githubusercontent.com/nikolaspay/pakla-hub/main/distribution/4.18.0/Pakla-Topluluk.png)

Çoklu rol, kanal/görünüm yetkileri, moderasyon hiyerarşisi korumaları, kişi bazlı kanal istisnaları ve canlı kategori izin mirası bu sürümde bulunur. Rol atama/oluşturma kurucuda kalır. DM sesli/görüntülü davetleri, arkadaş grupları ve süreli/süresiz sessize alma desteklenir. Yerel mikrofon testi, düşük kamera yükü ve görüşme bağlantı ölçümleri ayarlardadır.

Klipler, oyun/uygulama kitaplığı, yerel müzik, temizlik ve bağlantı araçları korunur. Temizlik seçerek yapılır; FPS veya internet hızı artışı garanti edilmez.

## Geliştirme durumu

Ses/görüntü/ekran paylaşımı beta: en fazla altı kişi, aynı anda bir ekran paylaşımı. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. İki istemcili sentetik medya testleri geçti; altı kişilik yük, gerçek kişisel kamera/mikrofon ve farklı ağ testleri tamamlanmadı. KLIPY ortak test kotası 100 çağrı/saat. Spotify OAuth yapılandırılmadı. Mesajlar uçtan uca şifreli değil. Windows yayıncı sertifikası yok; patch paketleri ayrı RSA-SHA256 imzasıyla doğrulanır.

[Doğrulama ve devam eden sınırlar](distribution/4.18.0/QUALITY-REPORT.md) · [Sürüm notları](distribution/4.18.0/RELEASE.md)

Destek: supportpakla@gmail.com
