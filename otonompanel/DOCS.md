# OtonomPanel

Home Assistant evinizi tarar, tablet için hazır bir panel kurar. Panel tabletin tarayıcısında çalışır; bu uygulama
yalnızca panel dosyalarını sunar ve Home Assistant girişini tabletlere taşır.

## Gereksinimler
- Home Assistant **2025.12** ya da üstü (panel ayarlarını Home Assistant'ın kendi deposunda saklar).
  Takvim ayrıntısındaki etkinlik listesi için 2026.5 ya da üstü.
- Tablet: Android'de Chrome 80 ya da üstü, iPad / iPhone'da iOS 14 ya da üstü.

## Kurulum
1. Uygulamayı kurun (**Kurulum**) ve başlatın (**Başlat**). **Kenar çubuğunda göster** açık kalsın.
2. Kenar çubuğundaki **OtonomPanel (Beta)**'yı açın ya da bir tarayıcıda `http://HA-ADRESİ:8098` adresine gidin.
3. **Home Assistant ile giriş yap**'a basın, **yönetici** kullanıcınızla girin. Kurulum yardımcısı evi tarar,
   cihazları odalara yerleştirir ve paneli Home Assistant'a kaydeder (bu adım için yönetici gerekir).

Bilgisayarınızda **OtonomPanel-Kurulum.html** dosyası varsa (çift tıklayarak açılır) bu adımları ve tablet bağlantısını
QR koduyla birlikte adım adım gösterir.

## Güncelleme
Yeni sürüm çıkınca Home Assistant **Ayarlar → Sistem → Güncellemeler**'de gösterir; **Güncelle**'ye basın ya da bu
uygulamanın **Bilgi** sekmesinde otomatik güncellemeyi açın. Ayarlarınız Home Assistant'ta durur, güncellemede
kaybolmaz. Açık tabletler yeni sürüme bir dakika içinde kendiliğinden geçer.

## Tablet
1. Home Assistant'ta tablet için ayrı bir kullanıcı açın: Ayarlar → Kişiler → Kullanıcılar → Kullanıcı ekle.
   **Yönetici yapmayın**; isterseniz "Yalnızca yerel ağdan giriş" seçeneğini açın.
2. Tablette `http://HA-ADRESİ:8098` adresini açın, bu kullanıcıyla bir kez giriş yapın. Android tabletler
   `homeassistant.local` adını çoğu zaman bulamaz: Home Assistant'ın IP adresini kullanın (Ayarlar → Sistem → Ağ).
3. Sayfayı ana ekrana ekleyin (Android Chrome: menü → Ana ekrana ekle; iPad Safari: Paylaş → Ana Ekrana Ekle).
   Panel oradan tam ekran açılır; sonraki açılışlarda giriş istenmez.
4. Tablet kaybolursa Home Assistant'ta tablet kullanıcısını devre dışı bırakın ya da silin; panel yeniden giriş ister.

Evdeki bütün tabletler aynı paneli görür; panelde yapılan düzenleme hepsine geçer.

## Lite ve Pro
Panel **Lite** olarak ücretsizdir: kurulum, bütün cihaz kartları ve pencereleri, ana ekran, şablon sayfalar
(Robot Süpürge, Medya, Güvenlik), 1 özel sayfa, alarm, kilit, kamera, panel kilidi, ekran koruyucu.

**Pro** henüz satışta değil; satışa çıktığında tek seferlik lisansla açılacak: sınırsız özel sayfa, Home Assistant etiketiyle sayfa, enerji akışı, 30 gün ve
1 yıl grafik, canlı grafik, başka odada çalma, grubun sesi, medya kısayolları, kartta görünen kaynaklar, panel
otomasyonları, uzun basma ve çift dokunma, koşullu kart, ek temalar, canlı hava arka planı, ekran koruyucuyu
özelleştirme, tablete özel görünüm.

- **Ücretsiz deneme:** Pro satışa çıktığında panelde 14 günlük ücretsiz deneme açılacak (ev başına bir kez). Lite'ı
  şimdi kuranlar da o zaman kullanabilecek.
- **Lisans anahtarı:** Ayarlar → Sürüm → "Lisans anahtarım var". Anahtar Home Assistant'ta saklanır; bir kez girmek
  evdeki bütün tabletler için yeter. Tablet sayısı sınırsız.
- Anahtar tablette doğrulanır; hiçbir sunucuya sorulmaz, internet gerekmez.
- Lisans kaldırılırsa ya da deneme biterse Pro ayarları **silinmez**, yalnız kullanılmaz; lisans girilince aynen
  geri gelir.

## Seçenekler
- `ha_adresi` (Yapılandırma sekmesi): Uygulamanın Home Assistant'a ulaştığı iç adres. Varsayılan `http://homeassistant:8123`.
  Yalnızca Home Assistant'ı farklı bir portta ya da adreste çalıştırıyorsanız değiştirin.
- `gunluk_seviyesi`: `debug`, `info`, `warning` ya da `error`. `debug` tabletlerin bilgi satırlarını da
  uygulamanın **Günlük** sekmesine yazar (sorun ararken kullanın).

## Gizlilik ve güvenlik
- Panel çalışmak için internete ihtiyaç duymaz ve kendiliğinden hiçbir yere veri göndermez. İki isteğe bağlı istisna:
  - Ayarlar → Gelişmiş → **Destek ve sorun bildir** bölümünden kendiniz bir talep gönderirseniz yazdığınız mesaj ve ekranda
    gördüğünüz tanı bilgisi OtonomEv'e gider (cihaz, oda ve kişi adları, adresler, şifreler ve anahtarlar gitmez).
  - Ayarlar → Gelişmiş → **Yeni sürümleri haber ver** anahtarını açarsanız (kapalı gelir) panel günde bir kez otonomev.com'dan
    yalnız son sürüm numarasını okur; eviniz ya da kurulu sürümünüzle ilgili bilgi göndermez. Uygulama olarak
    kurduysanız buna gerek yoktur: güncellemeyi Home Assistant kendisi bildirir.
  Ayrıntı: otonomev.com/gizlilik
- Kullanım koşulları ve lisans: Ayarlar → Gelişmiş → **Kullanım koşulları ve lisans** (paketteki `panel/LISANS.txt`).
- Panel ayarları ve lisans Home Assistant'ın
  kendi deposunda durur.
- 8098 portunu internete açmayın (port yönlendirme yapmayın). Uygulama giriş isteklerini yalnızca yerel ağdan iletir.
- Uygulama şifre ya da anahtar saklamaz; tabletin oturumu tarayıcısında durur ve Home Assistant'tan kapatılabilir.
- Tabletin giriş yenilemeleri Home Assistant'a uygulama üzerinden gider: HA'daki "son kullanım" adresi uygulamanın
  iç adresi görünür. HA'da `login_attempts_threshold` (IP engeli) kullanıyorsanız uygulama, aynı tabletten 15 dakikada
  5 başarısız denemeden sonra iletmeyi 15 dakika durdurur.

## Sorun giderme
- **Tablet "Bu tarayıcı OtonomPanel'i açamıyor" diyor:** tarayıcı çok eski. Chrome'u güncelleyin (Android) ya da
  iOS 14 ve üstü bir cihaz kullanın.
- **Tablet adresi açılmıyor:** `homeassistant.local` yerine Home Assistant'ın IP adresini deneyin; uygulamanın
  çalıştığını (Bilgi sekmesi) ve 8098 portunun açık olduğunu denetleyin.
- **Giriş sonrası "Oturum kapandı":** tablet kullanıcısı devre dışı ya da oturum Home Assistant'ta kapatılmış;
  yeniden giriş yapın.
- Tabletlerin uyarı ve hataları bu uygulamanın **Günlük** sekmesine yazılır.

## Bilinen sınırlar
- Home Assistant doğrudan HTTPS (kendi sertifikası) ile çalışıyorsa varsayılan iç adres `http://homeassistant:8123`
  çalışmaz; `ha_adresi` seçeneğini düzeltin.
- Home Assistant Container ya da Core kurulumlarında uygulama yoktur: panel `/config/www/otonompanel/` klasörüne
  kopyalanır ve `http://HA-ADRESİ:8123/local/otonompanel/index.html` adresinden açılır.

## Lisans
OtonomPanel'in kullanım koşulları ve Pro lisansı: [otonomev.com](https://otonomev.com).
