# Pakla Hub 4.15

Açılışta simge yenilemesi ve açılır menü kapanışından kaynaklanan çökme düzeltmeleri. Bannerlı topluluklar, kanal araması, kolay ses kanalı ekleme, rol bazlı kanal izinleri, DM sesli/görüntülü arama davetleri ve sohbet bazında sessize alma.

Arama için iki taraf da 4.15 kullanmalı. Ses/görüntü 6 kişilik beta; aynı anda bir ekran paylaşımı. TURN/SFU bulunmadığı için bazı ağlarda bağlantı kurulamayabilir. Kamera ve mikrofon kullanıcı açınca başlar. Bildirim tercihleri cihazda hesap bazında saklanır.

Patch RSA-SHA256 ile doğrulanır. Windows Authenticode sertifikası yapılandırılmadı.

Doğrulama: uygulama/kurulum testleri; imza, hash, bozulan paket ve dizin geçişi kontrolleri; kanal izinleri ve arama yetkileri için Supabase testleri; iki gerçek WebView2 istemcisi arasında sentetik ses/kamera/ekran aktarımı. Gerçek kullanıcı cihazlarında ve altı kişilik tam yükte test yapılmadı.
