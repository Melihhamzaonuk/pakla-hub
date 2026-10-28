# Topluluk kapsamı ve devam eden işler

28 Ekim 2026 · 4.19. Bu belge çalışan özelliklerle hedeflenen özellikleri ayırır. Discord özellik eşitliği tamamlanmış değildir; bağlantısız düğmeler veya örnek ekranlar tamamlanmış özellik sayılmaz.

| Alan | Pakla 4.19 durumu | Tamamlanacak iş |
|---|---|---|
| Sunucu şeridi / kanal dizini / üye paneli | Var; sosyal ekranlarda tek şerit, dar pencerede kanal-sohbet geçişi | Daha kapsamlı klavye ve ekran okuyucu denetimi |
| Sunucu oluşturma / şablon / kurallar | Var | Atomik başlangıç şablonu, onboarding ve kuralları yeniden kabul |
| Metin / duyuru / ses kanalı | Var; gerçek kayıt biçimi düzeltildi | Daha geniş sunucu kapasitesi için yük testleri |
| Kategoriler / arama / sıralama | Var; kanal konusu da aranır, yukarı/aşağı sıra | Sürükleyerek taşıma, kategori sıralama arayüzü |
| Özel kanal / çoğaltma | Eklendi; özel kanal normal üyeye görünmez; çoğaltma izinleri korur | Oluştururken rol/üye erişimi seçimi; sonradan izin düzenleyicisi mevcut |
| Kanal arşivi / geri açma | Var; mesajlar korunur | Ayrı arşiv tarayıcısı |
| Çoklu roller / renk / sıra | Var; kurucu oluşturur ve atar | Kurucu dışı Manage Roles delegasyonu, özel renkler/rol ikonları |
| Kanal ve kategori izinleri | Görme, mesaj, bağlanma, konuşma, yayın; rol ve kişi istisnaları, kategori mirası | Ayrıntılı mesaj/dosya/rol/davet/moderasyon yetkileri |
| Moderasyon hiyerarşisi | Alt role işlem korumaları, çıkarma/yasaklama mevcut | Timeout, süreli yaptırım, yasak listesi/itiraz ve ayrıntılı yetki delegasyonu |
| Yavaş mod | Eklendi; sunucuda uygulanır | Kalan süre sayacı ve mesaj yazarken daha ayrıntılı durum |
| Davetler | Yönetici kodu, süre/kullanım sınırı ve toplu iptal mevcut | Kişiye özel süre/kota seçimi, tekil davet listesi/iptali, bağlantı önizlemesi |
| Keşfet | Üye olunan/davetli ayrımı ve kurucunun açtığı genel sunucular | Kötüye kullanım raporlama, güvenli öneri/sıralama, daha geniş yük testleri |
| Mesaj geçmişi / arama / GIF / tepki / sabitler | Var | Yanıt/alinti zinciri, mesaj başına gerçek okunma durumu, daha geniş emoji desteği |
| Dosya / görsel yükleme | Yerel klipler ve GIF paylaşımı var | Sunucu sohbetine nesne depolama, kota, zararlı içerik denetimi ve erişim kontrollü dosya paylaşımı |
| DM / arkadaş grubu / arama daveti | Var; ses/görüntü beta | Daha kapsamlı cihaz/ağ/ses kararlılığı testleri |
| Ses / kamera / ekran paylaşımı | Beta; 6 kişi, bir ekran paylaşımı | TURN/SFU, gerçek cihaz ve farklı ağ testleri, büyük oda yük testleri |
| Bildirimler / sessize alma | DM, grup, topluluk ve kanal için süreli/süresiz; tümünü okundu eklendi | Mention-only, rol mention bastırma, kategori ve cihazlar arası eşitleme |
| Profil / banner / sunucu kimliği | Var | Sunucuya özel takma ad/profil, ayrıntılı çevrimiçi durumu |
| Denetim geçmişi | Son 100 yönetim işlemi; eksik istemci çağrısı düzeltildi | Filtre, sayfalama ve daha kapsamlı olay türleri |
| Forum / thread | Yok | Veri modeli, erişim ve arşiv politikası; liste ve konuşma akışı |
| Etkinlik / Stage | Yok | Etkinlik takvimi, RSVP, sahne konuşmacı/moderatör akışı |
| AutoMod / raporlama | Yok | Güvenli eşik, inceleme kuyruğu, yaptırım ve itiraz |
| Bot / webhook / slash komut | Yok | Yetkilendirilmiş geliştirici platformu, imza ve hız sınırları |
| Sunucu sahipliği / yedek / dışa aktarma | Kısıtlı; arşiv mevcut | Güvenli sahiplik devri, veri dışa aktarma, kurtarma akışı |
| Mobil / tarayıcı istemcisi | Yok | Ayrı istemci ve bildirim altyapısı |

Tasarım ve akış referansları: [Discord rol ve izinleri](https://support.discord.com/hc/en-us/articles/214836687-Discord-Roles-and-Permissions), [kategori/kanal izinleri](https://support.discord.com/hc/en-us/articles/206029707-Setting-Up-Permissions-FAQ), [bildirim ayarları](https://support.discord.com/hc/en-us/articles/215253258-Notifications-Settings-101), [forum kanalları](https://support.discord.com/hc/en-us/articles/6208479917079-Forum-Channels-FAQ). Bunlar hedef kapsamı tanımlar; Pakla'da uygulanmış olduğu anlamına gelmez.

Diğer açık işler: Spotify OAuth bağlantısı, KLIPY üretim erişimi, Authenticode yayıncı sertifikası, bağımsız güvenlik incelemesi ve kaynak kod lisansı. Mesajlar uçtan uca şifreli değildir. Kaynak arşivi özel taslak olarak tutulur; uygulama güncellemesi kaynak kodu halka açmaz.
