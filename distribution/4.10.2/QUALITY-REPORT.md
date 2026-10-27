# Pakla Hub 4.10.2 doğrulama

Windows olay kaydı ve eski derleme testi, HubHome içinde pencere işleyicisi oluşmadan BeginInvoke çağrısını doğruladı. Yenileme yalnızca işleyici hazırken sıraya alınır; kayıtlı hesabın açılışta geri yüklenmesi sonrasındaki mevcut Navigate akışı korunur.

- 4.10.0 opening crash reproduced: BeginInvoke before native handle in HubHome constructor path
- 4.10.2: three background-enabled constructors, pre-handle home navigation, actual Shown/tray initialization, 1.4s message loop and clean exits using isolated guest data
- 12 product pages x five requested sizes, workspace/search/filter/profile/sidebar fixtures passed
- 4.10 search/shared-content/bulk-clip feature fixture passed; video bytes unchanged
- App and installer self-tests and RSA patch tamper/traversal/downgrade/apply/rollback tests passed
- Original 4.10.0 engine verifies and applies 4.10.2, preserving fixture library and update receipt
- Installed 4.10.2 exact binary hash matches release; 21 user-data files unchanged except expected release history metadata

Bu tur yalnızca açılış düzeltmesi yapıldı. Önceki 4.10 özellikleri korunur. Gerçek kullanıcı mesajı, kayıt veya uzaktan GIF isteği yapılmadı. Kaspersky son 36 nesnede sıfır tespit, şüphe ve hata bildirdi. Authenticode sertifikası yok; patch ayrı RSA imzası ile doğrulanır.

Güncelleme bildirimi: yeni/eski/geçersiz sürümler, kapalı tercih, gizli pencere kuyruğu, daha yeni aday önceliği, aynı oturumda tekrar bastırma ve iki seçim dar pencere testinde geçti. Ön plan odak kontrolü korunur; otomasyon kullanıcı odağını zorla değiştirmez.