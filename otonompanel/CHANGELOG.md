# Değişiklikler

## 0.9.4 (Beta, 28 Kasım 2026)
- Telefon görünümü: panel telefonda tek sütun açılır, aşağı kaydırarak kullanılır; pencereler ekranı kaplar.
- Başka bir cihazda aç: Ayarlar'daki QR kodu telefonla okut, panel orada açılsın. QR, Home Assistant'ın evdeki IP
  adresini gösterir (".local" adını bulamayan cihazlar için).
- Sayfalar arasında ekranı sağa sola kaydırarak geçebilirsin.
- Görünüm ölçeği: Ayarlar → Görünüm'den yazıları ve kartları büyüt ya da küçült.
- Kurulum kolaylaştı: Home Assistant adresi kendiliğinden gelir, "Paneli kur" düğmesi hep görünür, ilk açılışta üç
  kısa ipucu çıkar.
- Dokunma alanları büyüdü; Geri tuşu ve Esc açık pencereyi kapatır; bağlantı koparsa üstte açık bir uyarı çıkar.
- Güncellemeden sonra Ayarlar'ın en üstünde "Bu sürümde yenilikler" listesi çıkar.
- Ayarlar sadeleşti: "Yeni sürümleri haber ver" Ayarlar → Gelişmiş'e taşındı (davranışı aynı).
- Düzeltme: oda penceresinde kartların alt kısmı kesilmiyor.
- Kullanım koşulları 2026-11-28.1 sürümüne güncellendi.

## 0.9.3 (Beta, 21 Kasım 2026)
- Canlı hava arka planı yenilendi: yağmur, sağanak, şimşek, kar, karla karışık yağmur, dolu, sis, rüzgâr, bulut ve
  yıldızlı gece artık gerçekçi ve derinlikli. Efekt kartların arkasında kalır, kartları örtmez.

## 0.9.2 (Beta, 21 Kasım 2026)
- Kurulum sihirbazının son adımı panelin tablette ya da başka bir tarayıcıda açılacağı adresi gösterir.

## 0.9.1 (Beta, 21 Kasım 2026)
- Düzeltme: panel kenar çubuğundan açıldığında "Home Assistant ile giriş yap" artık "Invalid redirect URI" vermiyor.
  Giriş sayfası tam pencerede açılır, girişten sonra kenar çubuğundaki panele geri dönülür.

## 0.9.0 (Beta, 21 Kasım 2026)
İlk yayın (beta). Hataları Ayarlar → Destek ve sorun bildir'den iletebilirsin.
- Kendiliğinden kurulan tablet paneli: kurulum yardımcısı evi tarar, cihazları odalara yerleştirir, yeni cihaz
  gelince paneli günceller.
- Ana ekran (odalar, özet, medya, hava, alarm), şablon sayfalar (Robot Süpürge, Medya, Güvenlik), özel sayfalar,
  düzenleme modu ve kart ayarları; bütün cihaz türleri için ayrıntı pencereleri.
- Home Assistant'ın kendi girişi: tablet ayrı kullanıcıyla bir kez giriş yapar; uygulama giriş isteklerini yerel
  ağda dar bir iletici üzerinden taşır.
- Lite ücretsiz ve süresiz. Pro yakında: satış başlayınca lisansla açılacak (ev başına, internetsiz doğrulama);
  o gün Lite kullanan herkes Pro'yu 14 gün ücretsiz deneyebilecek.
- Destek ve sorun bildir: mesaj ve kişisel veri içermeyen tanı bilgisi yalnız sen "Gönder"e basınca gider.
- İsteğe bağlı "Yeni sürümleri haber ver" (kapalı gelir).
- Panel internetten hiçbir şey yüklemez; ayarlar Home Assistant'ta saklanır, bütün tabletler eşitlenir.
- Tablet günlükleri uygulamanın Günlük sekmesinde.
