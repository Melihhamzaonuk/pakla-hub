# Pakla Hub 4.20 — 29 Ekim 2026

## Değişiklikler

- WebView2 mikrofon/kamera izni yalnızca güvenilir yerel HTTPS kökeninde, açık görüşmede veya süreli mikrofon testinde istenir. İzin penceresi olay geri çağrısından sonraya alınır, deferral tamamlanır. İzin kalıcı kaydedilmez. Şema, alan adı, port ve yol benzetmeleri reddedilir.
- Kayıtlı cihaz artık yoksa sistem varsayılanı bir kez denenir. İzin reddedilirse yeniden isteme döngüsü yoktur. Eski cihazın kapanma olayı yeni cihazı kapatmaz. Kamera karşı taraf bağlantısı hazırlanırken de açılabilir.
- Ekran paylaşımı: ekonomi 720p/10, dengeli 720p/30, detay 1080p/15, akıcı 1080p/30 hedefleri. Gerçek kalite ağ ve cihazla sınırlıdır. Yayın sırasında kaynak/kalite değişir; iptal eski yayını korur, gönderici hatasında geri alınır. Ekran sesi eklenmedi.
- DM araması sohbet içinde açılır, mesaj yazma alanı kalır. Geri dön, kabul, reddetme ve bitirme akışları düzenlendi. Dahili görüşme odaları sunucu listesinden/aramasından gizlenir; gerçek arkadaş grupları korunur.
- Nick ve benzersiz @kullanıcı adı ayrı alanlar. DM ve gelen arama kimliği @adı da gösterir. Benzersizlik sosyal profil etkinleştirme/kaydetme sırasında uygulanır; kayıt metadata'sı rezervasyon değildir.

## Doğrulama

- Gerçek WebView2 motoru ve Chromium sahte cihazları: izin verme/reddetme, güvenilir köken denetimi, mikrofon/kamera açılması veya kapalı kalması. Fiziksel cihazlar kullanılmadı.
- İki gerçek yerel WebRTC istemcisi: sentetik ses, kamera ve ekran aynı anda aktarıldı; iki yönde ayrı kamera/ekran sayaçları 1000 baytı geçti. Yeniden bağlantı, yalnız kamera kapatma ve tüm sentetik izlerin durması doğrulandı.
- JS regresyonları: eski cihazın varsayılana geçmesi, izin reddi, cihaz bitişi, geç izin yanıtı, paylaşım seçimini iptal, kaynak değiştirme, canlı çözünürlük/FPS/bitrate ve kapatma.
- Derlenmiş istemci + sahte HTTP: DM daveti/kabul/ayrılma, sohbet içinde kalma, özel odanın sunucu listesine çıkmaması, bildirim susturma ve hesap ayrımı. Menü kapatma sonrası kaynak temizliği 30 tekrar; kısa zamanlama varsayımı yerine 1 saniyelik sınırlı bekleme kullanıldı.
- Kanal oluşturma/kategori/rol/izin ve kayıt-yenileme yarışları yeniden test edildi. 344–1440 mantıksal genişlikler ve %150 ölçek denetlendi. Tüm trafik fixture hedeflerine gitti.
- Canlı Supabase üzerinde transaction içinde geçiş iki kez uygulandı: özel arama işareti, gerçek grubun korunması, yabancı kullanıcının erişim reddi, aynı nickin kabulü ve büyük/küçük harften bağımsız benzersiz kullanıcı adı. Test kullanıcıları rollback ile geri alındı. Ardından doğrulanan geçiş canlıya uygulandı.

## Sınırlar

Gerçek fiziksel mikrofon/kamera, farklı ağlar ve altı kişilik yük testi tamamlanmadı. Ses/görüntü beta: altı kişi, aynı anda tek ekran. TURN/SFU yok; bazı ağlarda bağlantı kurulamayabilir. Ekran sesi yok. Discord ile özellik eşitliği yok.

KLIPY ortak test kotası ve Spotify OAuth eksikleri sürer. Mesajlar uçtan uca şifreli değildir. Authenticode yayıncı sertifikası yok; patch RSA-SHA256 imzası ayrıdır. Antivirüslerde sıfır uyarı veya ağ/FPS artışı garantisi verilmez.

Kaynak paketi özel taslaktır; yeniden kullanım lisansı seçilmedi ve kaynaklar halka açılmadı. Önceki sürümlerin ayrıntılı topluluk sınırları TOPLULUK-YOL-HARITASI.md dosyasındadır. Yayının son doğrulaması release-verification.json içindedir.

WebView2 olay modeli: https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/threading-model
