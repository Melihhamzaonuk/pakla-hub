# Pakla Hub 4.9 kontrol raporu

27 Ekim 2026. Windows x64 / .NET Framework 4.8.

## Yeni akışlar

Native 1366×900 pencerede, sahte HTTP sunucusu ve geçici dosyalarla doğrulandı:

- Hesaba özel sohbet sabitleme, sağ tıkla kaldırma, kalıcı ayarlar ve okunmamış filtresi. Filtre, editör nesnesini ve taslağı korur.
- Gelen kutusu: mesaj/istek/kanal sayıları, global rozetler, okunmuş sohbetin kalkması ve kanalın güncel konumda açılması. İçerik değişmediğinde odaktaki düğmeler yeniden oluşturulmaz.
- Geri/ileri: sohbet bağlamı ve taslağı, yeni gezinmede ileri dalının silinmesi, en fazla 40 bellek içi kayıt ve hesap değişiminde temizlenmesi.
- Klip koleksiyonu: sahip hesabın filtreleri, ad/koleksiyon kaydetme ve metadata yeniden yükleme. Diğer hesabın koleksiyonları görünmez. Video dosyasındaki test baytları değişmedi.
- Hesap değişimi: eski klibin düzenlenmesinin reddi, eski özel görünümün temizlenmesi, açık diyalog iptali, pin/filtre/geçmiş yalıtımı ve kayıt sahibinin korunması. Gerçek kayıt başlatılmadı; kayıt sahibi durumu model üzerinde kontrol edildi.
- Geç gelen sosyal yanıtın nesil değişiminden sonra reddi ve çevrimdışı gelen kutusunun yükleniyor durumunda takılmaması.

## Görünüm ve regresyon

12 ekran, beş istenen pencere boyutunda kontrol edildi: Ana Sayfa, Mesajlar, Topluluklar, Gelen Kutusu, Sunucu Keşfet, Klipler, Kayıt Ayarları, Kitaplık, Araçlar, Profil, Ayarlar ve Müzik. Minimum pencere sınırı geçerlidir. Native 144 DPI ve test ölçeğiyle 96/192 DPI kullanıldı; fiziksel monitör değiştirilmedi. Başlık sınırları/çakışma, dar bölüm menüsü, filtreler, profil sekmeleri, arama komutu ve kaydedilen sohbet genişliği geçti.

Önceki keşif, taslak, alıntı, mesaj arama, tepki/düzenleme/sabit, kanal yalıtımı, yeniden deneme nonce'ı, oturum DPAPI/çevrimdışı/yenileme/iptal/çıkış yarışı testleri geçti. HTTP testleri gerçek kişilere mesaj göndermedi.

Uygulama özellik/yerel veri testleri, kurulum dosya özetleri/simge/kısayol/yeniden kurulum/veri koruma, RSA patch doğrulama, bozulmuş paket/yol taşması/eski sürüm reddi ve geri alma testleri geçti. 2.1, 4.3 ve 4.8 güncelleyicilerinden 4.9 kurulumu doğrulandı.

Son uygulama, kurulum, güncelleyici ve patch Kaspersky ile tarandı: 28 nesne, 0 tespit, 0 şüphe, 0 hata.

## Sınırlar

Görseller test verisidir. Gerçek kayıt, video dışa aktarma/silme, oyun açma veya gerçek kişilere mesaj gönderme yapılmadı. Farklı ağlarda gerçek ses/ekran paylaşımı testi tamamlanmadı. Ses beta 6 kişi ve tek paylaşımla sınırlıdır; TURN/SFU yoktur. KLIPY üretim erişimi, Spotify OAuth ve güvenilir Windows yayıncı sertifikası henüz yoktur. Mesajlarda uçtan uca şifreleme bulunmaz. Bu rapor tüm hataların bittiği iddiası değildir.