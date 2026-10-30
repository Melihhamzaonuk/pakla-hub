Pakla Hub 4.27.0 — hata düzeltmeleri ve görsel tutarlılık

DÜZELTİLENLER
- Yuvarlak düğmeler sabit koyu renk yerine altlarındaki gerçek yüzeyi çizer. Renk geçişleri üzerinde köşelerde kalan koyu dikdörtgenler kaldırıldı. Ortak düğme tabanı 17 kontrol türüne uygulandı.
- Küçük yuvarlak şekillerde köşe yarıçapı boyutu aşmayacak şekilde sınırlandı; taşan ve kendiyle kesişen eğriler engellendi.
- Araç çubuğu simgeleri 20 mantıksal birime alındı; metinsiz düğmelerde kare yüzey ve yatay/dikey ortalama kullanılır. Sunucu ve kişi simgelerinin dikey hizası düzeltildi. Klip favori düğmesi artık doğrudan küçük resmin yüzeyinde bulunur.
- Klip favorileri ve toplu favori işlemi aynı galeride güncellenir; arama ve sıralama sıfırlanmaz. Kaydetme hatasında favori durumu geri alınır; sahiplik kontrolü korunur.
- Klip seçenekleri menüsünün komşu kartların altında kalması düzeltildi. Dışarı tıklama ve Esc ile kapanır; aynı anda yalnızca bir menü açık kalır.
- Klip hazırlanırken veya uygulama içi panel açıkken geri/ileri geçmişi hatalı ilerlemez.
- VPN bağlantı düğmesi hızlı çift tıklamaya karşı korunur. Bağlantı kesme zaman aşımında yardımcı işlem bırakılmaz. VPN hızlı arama sonuçlarına eklendi.
- İşlem düğmeleri dar ekranda sıkışmak yerine alt satıra geçer. Dar VPN başlığına daha fazla yer ayrıldı.
- Geçersiz klip süre/boyut verilerinin çizimi bozması engellendi; geçersiz içe aktarma süresi reddedilir.
- Ana sayfa yeni karşılama alanı ve değiştiğinde yenilenen gerçek klip/kayıt/mesaj durum kartları içerir. Karşılama hareketi yaklaşık dört saniye sonra durur; sürekli boşta çizim yapmaz.
- Önceki tepsiye küçültme, ayrı Tamamen çık ve mor/mint klip tasarımı korunur.

DOĞRULAMA
- 35 ekran, üç pencere genişliğinde tarandı: 105 ekran/genişlik birleşimi. Düğme envanteri ve gerçek güvenli tıklama sayısı button-audit.txt / button-inventory.tsv dosyalarındadır. Envanter sayısı benzersiz düğme sayısı değildir.
- Gerçek WebView2 içindeki favori tıklaması native köprüden geçirilerek yerel test verisine kaydedildi; aynı galeri, arama ve sıralamanın korunduğu doğrulandı.
- Klip galerisinin filtreleri, sıralaması, favorileri, toplu seçim/temizleme, kayıt komutları, ayarlar, içe aktarma komutu, düzenleme/dışa aktarma komutları, sayfalama, menü tıklanabilirliği, dar görünüm ve hareket azaltma kontrolleri geçti.
- Klip düzenleme paneli boş başlık doğrulaması, kaydetme ve vazgeçme; hızlı arama sonucu açma; lisans/kısayol panellerinde Esc; favori kaydetme ve geri alma; engellenen gezinme; tepsi/geri açma/tam çıkış; kurulum otomatik kapanma testleri geçti.
- Dokuz yuvarlak düğme türünün dört köşesi %100 ve %150 ölçekte altındaki renk geçişiyle karşılaştırıldı: 72 piksel kontrolü. Görsel kontrol sayfaları icon-surfaces-96dpi.png ve icon-surfaces-144dpi.png.

SINIRLAR
Gerçek iki hesapla mesaj gönderme, gerçek VPN bağlantısı açma, kişisel ekran/mikrofon kaydı, kaldırma, gerçek dosya temizleme ve Windows başlangıç ayarlarını değiştirme bu çalışmada otomatik tıklanmadı. Bunlar raporda ayrı işaretlendi; bütün canlı servis işlemlerinin başarılı olduğu iddia edilmez. Ana sayfa ve sohbet görsellerindeki klip/mesajlar gösterim verisidir. Karşılaştırmalı CPU/RAM ölçümü yapılmadı.

Kurulum ve RSA imzalı güncelleme paketi yayımlanmıştır. Kaynak kodları özel depoda tutulur. Kurulu kullanıcı kopyası bu yayın işlemiyle doğrudan değiştirilmedi. Windows yayıncı imzası içermez; güncelleme RSA imzası ayrı mekanizmadır. Yeni paket ve gerçek 4.23 güncelleme motoruyla imza, bozuk paket reddi, uygulama, geri alma ve veri koruma testleri geçti.
