# Pakla Hub 4.7 kontrol raporu

Tarih: 27 Ekim 2026. Windows x64 / .NET Framework 4.8.

Bu sürümde doğrulananlar:

- Keşif: yükleme sırasında eski kartların temizlenmesi, boş sonuç, hata/yeniden deneme, ters sırayla dönen iki isteğin doğru sonucu koruması.
- Sohbet: yukarıda okurken yeni mesajın kaydırmaması, yeni mesaj düğmesi, odak dışındayken okundu gönderilmemesi, geçersiz/null kayıtların elenmesi ve eski hesap neslinin yanıtının reddi.
- Sunucu: geçmiş imlecinin geçişte sıfırlanması; dar penceredeki menüden sabitlerin gerçekten açılması.
- Taslak: dolu kutuda ekleme reddi, seçili metnin sınır içinde değiştirilmesi ve salt okunur kutunun korunması.
- Gönderim: yeniden deneme nonce'ı, kanal yalıtımı, bekleyen işlem ve sayfa geçişinde taslak korunması.
- Medya izinleri: çift mikrofon isteğinin birleştirilmesi, izin yanıtı gelmeden ayrılıp tekrar bağlanmada eski ses/ekran kaynaklarının durdurulması. Bu testler sahte medya nesneleri kullandı.
- Ses katılımı: bekleyen katılım iptal edilince sunucudaki oturuma leave gönderilmesi ve geç yanıtın mevcut görünüme iletilmemesi. HTTP testi sahte sunucu kullandı.
- Gerçek WebView2: başlatma, simüle edilen süreç hatasında izin durumunun kapanması ve yeniden başlatmayla ready olayı. Mikrofon/ekran istenmedi.
- Gerçek WebRTC: iki görünüm arasında DTLS ile sentetik osilatör sesi ve canvas videosu aktarımı.
- Oturum: DPAPI kayıt/yeniden başlatma, çevrimdışı geri dönüş, token yenileme/iptali, beni hatırlama kapalı ve çıkış sırasında yenileme yarışı. HTTP test sunucusu kullanıldı.
- Görünüm: yedi sayfa, beş istenen pencere boyutu; uygulamanın minimum boyut sınırı geçerlidir. Yerel 144 DPI düzeni ve kompakt mesaj çubuğu kontrol edildi.
- Kurulum: gömülü dosyalar/özetleri, simge/kısayol, yeniden kurulum ve kullanıcı verilerinin korunması.
- Patch: RSA, özet, bozulmuş paket/yol taşması/eski sürüm reddi, uygulama ve geri alma. 2.1, 4.3 ve 4.6 güncelleyicileriyle 4.7 kurulumu test edildi.
- Antivirüs: son uygulama, kurulum, güncelleyici ve patch Kaspersky ile tarandı; 28 nesne, 0 tespit, 0 şüphe, 0 hata.

Gizli WebView testlerinde bazı başlatmalar zaman aşımına uğradı. Kontrol tanıtıcılarını açıkça oluşturan yeniden başlatma testi ve iki görünüm testi geçti. Bu sonuçlar tüm ağlarda gerçek mikrofon/ekran paylaşımının çalıştığını kanıtlamaz.

Açık altyapı sınırları: TURN/SFU, KLIPY üretim erişimi, Spotify OAuth ve güvenilir Windows yayıncı sertifikası henüz yoktur. Gerçek kullanıcılarla farklı ağlarda ses/ekran denemesi ayrıca gereklidir. Bu rapor tüm hataların bittiği iddiası değildir.