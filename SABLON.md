# DKC AI Labs - Sayfa Şablonları

## Klasör Yapısı

```
android/
└── oyun-adi/
    ├── index.html          (Oyun detay sayfası)
    ├── privacy.html        (Gizlilik politikası)
    └── images/
        ├── icon.png        (Oyun ikonu)
        └── screenshots/
            ├── s1.png
            ├── s2.png
            └── s3.png
```

## Yeni Oyun Eklerken Yapılacaklar

1. `android/oyun-adi/` klasörü oluştur
2. `android/oyun-adi/index.html` oluştur (Detay Şablonu)
3. `android/oyun-adi/privacy.html` oluştur (Gizlilik Şablonu)
4. `index.html` ana sayfaya oyun kartını ekle (Oyunlar bölümü - alfabetik sıra)
5. `index.html` ana sayfaya gizlilik kartını ekle (Gizlilik bölümü - alfabetik sıra)
6. `index.html` hakkımızda bölümündeki oyun sayısını güncelle

---

## 1. Oyun Detay Sayfası Şablonu (android/oyun-adi/index.html)

> Değiştirilecek yerler: OYUN_ADI, OYUN_ACIKLAMA, OYUN_TAGLINE, OYUN_EMOJI, BADGE_TIPI, CTA_BOLUMU, OZELLIKLER

```html
<!DOCTYPE html>
<html lang="tr" data-theme="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OYUN_ADI - DKC AI Labs</title>
    <meta name="description" content="OYUN_ADI - OYUN_TAGLINE">
    <link rel="icon" type="image/png" href="../../assets/images/imzalogo.png">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

    <!-- CSS -->
    <link rel="stylesheet" href="../../assets/css/style.css">
</head>
<body>
    <div class="bg-effects">
        <div class="bg-orb bg-orb-1"></div>
        <div class="bg-orb bg-orb-2"></div>
    </div>

    <nav>
        <div class="nav-container">
            <a href="../../index.html#oyunlar" class="back-btn">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z"/></svg>
                Geri Dön
            </a>
            <a href="../../index.html" class="logo-text">DKC AI Labs</a>
        </div>
    </nav>

    <main class="game-detail-container">
        <div class="game-detail-header">
            <div class="game-icon">
                <img src="images/icon.png" alt="OYUN_ADI" onerror="this.parentElement.innerHTML='OYUN_EMOJI'">
            </div>
            <div class="game-badges">
                <!-- BADGE_TIPI: badge-testing veya badge-soon -->
                <span class="badge BADGE_TIPI">Kapalı Test</span>
            </div>
            <h1>OYUN_ADI</h1>
            <p class="tagline">OYUN_TAGLINE</p>
        </div>

        <div class="game-screenshots">
            <div class="screenshots-grid">
                <div class="screenshot-item">
                    <img src="images/screenshots/s1.png" alt="Ekran Görüntüsü 1" onerror="this.parentElement.innerHTML='Görsel Eklenecek'">
                </div>
                <div class="screenshot-item">
                    <img src="images/screenshots/s2.png" alt="Ekran Görüntüsü 2" onerror="this.parentElement.innerHTML='Görsel Eklenecek'">
                </div>
                <div class="screenshot-item">
                    <img src="images/screenshots/s3.png" alt="Ekran Görüntüsü 3" onerror="this.parentElement.innerHTML='Görsel Eklenecek'">
                </div>
            </div>
        </div>

        <div class="game-description">
            <h2>Oyun Hakkında</h2>
            <p>OYUN_ACIKLAMA_1</p>
            <p>OYUN_ACIKLAMA_2</p>
        </div>

        <div class="game-features">
            <h2>Özellikler</h2>
            <div class="features-list">
                <div class="feature-item">
                    <span class="feature-icon">✨</span>
                    <div>
                        <h4>Modern Tasarım</h4>
                        <p>Sade ve şık arayüz</p>
                    </div>
                </div>
                <div class="feature-item">
                    <span class="feature-icon">🎨</span>
                    <div>
                        <h4>Çeşitli Temalar</h4>
                        <p>Farklı görsel deneyimler</p>
                    </div>
                </div>
                <div class="feature-item">
                    <span class="feature-icon">📶</span>
                    <div>
                        <h4>Çevrimdışı</h4>
                        <p>İnternet gerektirmez</p>
                    </div>
                </div>
                <div class="feature-item">
                    <span class="feature-icon">🔋</span>
                    <div>
                        <h4>Düşük Pil</h4>
                        <p>Optimize edilmiş performans</p>
                    </div>
                </div>
                <div class="feature-item">
                    <span class="feature-icon">🎮</span>
                    <div>
                        <h4>OZEL_OZELLIK</h4>
                        <p>OZEL_OZELLIK_ACIKLAMA</p>
                    </div>
                </div>
                <div class="feature-item">
                    <span class="feature-icon">👨‍👩‍👧‍👦</span>
                    <div>
                        <h4>Tüm Yaşlar</h4>
                        <p>Aile dostu içerik</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- CTA: Kapalı Test / Yayında -->
        <div class="game-cta">
            <h3>Hemen İndir!</h3>
            <p>OYUN_ADI şimdi Google Play'de! Ücretsiz indirin ve oynamaya başlayın.</p>
            <div class="cta-buttons">
                <a href="https://play.google.com/store/apps/details?id=APP_ID_BURAYA" class="btn btn-primary" target="_blank">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M3.609 1.814L13.792 12 3.61 22.186a.996.996 0 01-.61-.92V2.734a1 1 0 01.609-.92zm10.89 10.893l2.302 2.302-10.937 6.333 8.635-8.635zm3.199-3.198l2.807 1.626a1 1 0 010 1.73l-2.808 1.626L15.206 12l2.492-2.491zM5.864 2.658L16.8 9.99l-2.302 2.302-8.634-8.634z"/></svg>
                    Google Play'den İndir
                </a>
            </div>
        </div>

        <!-- CTA: Yakında (alternatif)
        <div class="game-cta">
            <h3>Yakında Yayında!</h3>
            <p>OYUN_ADI şu anda geliştirme aşamasında. Çok yakında Google Play'de!</p>
            <div class="cta-buttons">
                <button class="btn btn-disabled" disabled>Yakında</button>
            </div>
        </div>
        -->
    </main>

    <button class="scroll-top" id="scrollTop" aria-label="Yukarı çık">
        <svg viewBox="0 0 24 24" fill="white"><path d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z"/></svg>
    </button>

    <script src="../../assets/js/main.js"></script>
</body>
</html>
```

---

## 2. Gizlilik Politikası Şablonu (android/oyun-adi/privacy.html)

> Değiştirilecek yer: OYUN_ADI

```html
<!DOCTYPE html>
<html lang="tr" data-theme="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gizlilik Politikası - OYUN_ADI | DKC AI Labs</title>
    <meta name="description" content="OYUN_ADI oyunu için gizlilik politikası">
    <link rel="icon" type="image/png" href="../../assets/images/imzalogo.png">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

    <!-- CSS -->
    <link rel="stylesheet" href="../../assets/css/style.css">
</head>
<body>
    <div class="bg-effects">
        <div class="bg-orb bg-orb-1"></div>
        <div class="bg-orb bg-orb-2"></div>
    </div>

    <nav>
        <div class="nav-container">
            <a href="../../index.html#gizlilik" class="back-btn">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z"/></svg>
                Geri Dön
            </a>
            <a href="../../index.html" class="logo-text">DKC AI Labs</a>
        </div>
    </nav>

    <main class="privacy-container">
        <div class="privacy-header">
            <h1>OYUN_ADI</h1>
            <p class="subtitle">Gizlilik Politikası</p>
            <span class="badge">Android Uygulaması</span>
        </div>

        <div class="privacy-content">
            <h2>Toplanan Veriler</h2>
            <p>OYUN_ADI, kullanıcılardan kişisel veri toplamamaktadır. Oyun tamamen çevrimdışı çalışır ve hesap oluşturma gerektirmez.</p>

            <h2>Reklamlar</h2>
            <p>Uygulamamız Google AdMob aracılığıyla reklam göstermektedir. AdMob, reklam deneyimini kişiselleştirmek için cihaz tanımlayıcıları ve kullanım verileri toplayabilir. Daha fazla bilgi için <a href="https://policies.google.com/privacy" target="_blank">Google Gizlilik Politikası</a> sayfasını inceleyebilirsiniz.</p>

            <h2>Yerel Depolama</h2>
            <p>Oyun ilerlemeniz ve ayarlarınız (ses, tema tercihleri, en yüksek skor vb.) yalnızca cihazınızda yerel olarak saklanır ve hiçbir sunucuya gönderilmez.</p>
            <p>Uygulamayı sildiğinizde tüm oyun verileriniz (skorlar, ayarlar) kalıcı olarak silinecektir.</p>

            <h2>Çocukların Gizliliği</h2>
            <p>Uygulamamız, çocuklara yönelik uygunsuz içerik barındırmaz ve kişisel bilgi toplamaz. Ayrıca, uygulamamızda yer alan reklamlardan sorumlu değiliz; reklam sağlayıcının politikaları farklı olabilir.</p>

            <h2>İletişim</h2>
            <p>Sorularınız için bizimle iletişime geçebilirsiniz:</p>
            <p><strong>E-posta:</strong> <a href="mailto:dkcailabs@gmail.com">dkcailabs@gmail.com</a></p>

            <h2>Değişiklikler</h2>
            <p>Bu gizlilik politikası zaman zaman güncellenebilir. Değişiklikler bu sayfada yayınlanacaktır.</p>

            <div class="update-date">
                Son güncelleme: 3 Ocak 2025
            </div>
        </div>
    </main>

    <button class="scroll-top" id="scrollTop" aria-label="Yukarı çık">
        <svg viewBox="0 0 24 24" fill="white"><path d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z"/></svg>
    </button>

    <script src="../../assets/js/main.js"></script>
</body>
</html>
```

---

## 3. Ana Sayfa Oyun Kartı (index.html - Oyunlar bölümü)

> Alfabetik sıraya göre ekle

### Kapalı Test / Yayında olan oyun:
```html
<!-- OYUN_ADI -->
<div class="game-card animate-on-scroll">
    <span class="badge badge-testing">Kapalı Test</span>
    <div class="game-image">
        <img src="android/OYUN_KLASOR/images/icon.png" alt="OYUN_ADI" onerror="this.parentElement.innerHTML='<span class=\'placeholder-icon\'>OYUN_EMOJI</span>'">
    </div>
    <div class="game-info">
        <h3>OYUN_ADI</h3>
        <p>OYUN_KISA_ACIKLAMA</p>
        <span class="platform">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M17.523 2c1.89.14 3.73 1.23 4.477 3.03.43 1.12.39 2.32.39 3.51v6.93c0 1.19.04 2.4-.39 3.52-.75 1.8-2.59 2.88-4.48 3.02H6.48c-1.89-.14-3.73-1.22-4.48-3.02-.43-1.12-.39-2.33-.39-3.52V8.54c0-1.19-.04-2.39.39-3.51C2.75 3.23 4.59 2.14 6.48 2h11.04zm-5.48 6.32L9.5 12l2.55 3.68h1.41L11 12l2.46-3.68h-1.41z"/></svg>
            Android
        </span>
    </div>
    <div class="game-actions">
        <a href="android/OYUN_KLASOR/" class="btn btn-primary">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M12 4.5C7 4.5 2.73 7.61 1 12c1.73 4.39 6 7.5 11 7.5s9.27-3.11 11-7.5c-1.73-4.39-6-7.5-11-7.5zM12 17c-2.76 0-5-2.24-5-5s2.24-5 5-5 5 2.24 5 5-2.24 5-5 5zm0-8c-1.66 0-3 1.34-3 3s1.34 3 3 3 3-1.34 3-3-1.34-3-3-3z"/></svg>
            İncele
        </a>
    </div>
</div>
```

### Yakında olan oyun:
```html
<!-- OYUN_ADI -->
<div class="game-card animate-on-scroll">
    <span class="badge badge-soon">Yakında</span>
    <div class="game-image">
        <img src="assets/images/yakinda.png" alt="OYUN_ADI" onerror="this.parentElement.innerHTML='<span class=\'placeholder-icon\'>OYUN_EMOJI</span>'">
    </div>
    <div class="game-info">
        <h3>OYUN_ADI</h3>
        <p>OYUN_KISA_ACIKLAMA</p>
        <span class="platform">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M17.523 2c1.89.14 3.73 1.23 4.477 3.03.43 1.12.39 2.32.39 3.51v6.93c0 1.19.04 2.4-.39 3.52-.75 1.8-2.59 2.88-4.48 3.02H6.48c-1.89-.14-3.73-1.22-4.48-3.02-.43-1.12-.39-2.33-.39-3.52V8.54c0-1.19-.04-2.39.39-3.51C2.75 3.23 4.59 2.14 6.48 2h11.04zm-5.48 6.32L9.5 12l2.55 3.68h1.41L11 12l2.46-3.68h-1.41z"/></svg>
            Android
        </span>
    </div>
    <div class="game-actions">
        <button class="btn btn-disabled" disabled>Yakında</button>
    </div>
</div>
```

---

## 4. Ana Sayfa Gizlilik Kartı (index.html - Gizlilik bölümü)

> Alfabetik sıraya göre ekle

```html
<a href="android/OYUN_KLASOR/privacy.html" class="privacy-card animate-on-scroll">
    <div class="text-content">
        <h4>OYUN_ADI</h4>
        <span>Android • Gizlilik Politikası</span>
    </div>
</a>
```

---

## Badge Tipleri
- `badge-testing` = Kapalı Test (turuncu)
- `badge-soon` = Yakında (koyu mavi)
- `badge-live` = Yayında (yeşil)

## Mevcut Oyunlar (Alfabetik)
| Oyun | Klasör | Durum |
|------|--------|-------|
| Altın Peşinde | altin-pesinde | Kapalı Test |
| Block Crush: Cubix | block-crush-cubix | Kapalı Test |
| Block Puzzle+ | block-puzzle-plus | Kapalı Test |
| Bricks Breaker | bricks-breaker | Yakında |
| Kelimeler ile TÜRKİYE | kelimeler-turkiye | Yakında |
| Rust Hunt | rust-hunt | Yakında |
| Target: Core | target-core | Kapalı Test |