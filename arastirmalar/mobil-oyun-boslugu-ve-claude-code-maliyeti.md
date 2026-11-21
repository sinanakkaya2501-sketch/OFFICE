# Mobilde hangi oyun eksik, Claude Code ile yapmak neye mal olur?

> Ofis zinciri: **Ece** (pazar araştırması) → **Kaan** (oyun fikri) → **Mert** (süre ve token tahmini). Görevi ofis yerine Claude yürüttü, 21 Kasım 2026.
> Durum: **kısa araştırma, karar Patron'da.** "Tahmin" yazan her şey ölçüm değil, varsayımdır.

## Kısaca

- **Kesin bir "boş tür" yok.** Pazar doymuş durumda: 2025'te indirmeler üst üste ikinci yıl düştü (%-7,2), gelir yerinde sayıyor ve para birkaç büyük türde (strateji, nişancı, bulmaca) toplanıyor. Bu türlerde küçük bir stüdyonun devlerle yarışması gerçekçi değil.
- **Asıl boşluk bir tür değil, bir tarz:** **reklamı rahatsız etmeyen, internetsiz, özenli ve sakin oyunlar.** Oyuncuların %52'si üst üste rahatsız edici reklam görünce oyunu bırakacağını söylüyor. Reklamsız, tek seferlik ücretli (premium) mobil oyun çıkışları 2025'te %77 arttı ama hâlâ indirmelerin sadece %4'ü. Yani talep var, rakip az. KIVILCIM zaten bu tarzda.
- **Türkiye'ye özel fırsat (tahmin):** Kaliteli, **günlük, internetsiz bir Türkçe kelime bulmacası.** Kelimelik çevrim içi ve rekabet odaklı; Wordle Türkçe çoğunlukla tarayıcıdan oynanıyor. Mağazada "günde bir bulmaca, sakin, Türkçe" boşluğu görünüyor. Bunu kesinleştirmek için mağaza indirme verisine (AppMagic / Sensor Tower) bakmak gerek.
- **Önerilen ilk oyun:** Günlük Türkçe kelime bulmacası. Claude Code ile **yaklaşık 3-5 haftada** (yarı zamanlı) mağazaya hazır hale gelir. **Max 5x planı (ayda 100 dolar) tek ay** büyük ihtimalle yeter (tahmin).
- **Dikkat:** Zamanın en büyük kısmını kod değil, **içerik** (kelime listesi, bulmacalar), görsel, ses ve gerçek telefonlarda test alır. Claude Code kodu hızlandırır, bunları yapmaz.

---

## 1. Ece: pazar araştırması

### Dünya pazarı (2025-2026)
| Bulgu | Sayı | Kaynak |
|---|---|---|
| Mobil oyun indirmeleri düşüyor | 2025'te %-7,2, 50,4 milyar | [Sensor Tower, State of Gaming 2026](https://gamedevreports.substack.com/p/sensor-tower-state-of-gaming-2026) |
| Gelir yerinde sayıyor | Uygulama içi satın alım 81,75 milyar $ (+%1,3) | aynı kaynak |
| En çok büyüyen türler | Strateji, nişancı, bulmaca (Royal Match, Last War gibi devler sürüklüyor) | aynı kaynak; [PocketGamer.biz](https://www.pocketgamer.biz/games-revenue-growth-stalls-in-2025-as-strategy-emerges-as-the-fastest-growing-genre) |
| 2026 ilk yarı | Gelir %-2 (~40 milyar $), indirme %-12 | [Tech Insider](https://tech-insider.org/mobile-game-revenue-decline-2026/) (Sensor Tower verisine dayanıyor) |
| İlk 300 oyunun yarısından fazlası 2024 öncesi çıkmış | Yeni oyunun öne çıkması zor | [PocketGamer.biz](https://www.pocketgamer.biz/puzzle-games-rise-as-mobile-genres-compete-for-attention-in-2026/) |

### Reklamsız ve ücretli oyunlar
- Premium (tek seferlik ücretli) mobil oyun çıkışları 2025'te **%77 arttı**, ~750 oyuna çıktı. Ücretsiz oyunlar yine de indirmelerin **%96'sını** alıyor. ([Pocket Tactics](https://www.pockettactics.com/premium-mobile-games-increase), AppMagic verisi)
- Balatro tek başına mobilde ~21 milyon $ kazandı. Ama Balatro hariç tutulduğunda da büyüme sürüyor. ([gamedev.net](https://gamedev.net/news/4367/))
- Uyarı: 2022'de de benzer bir sıçrama olmuş, 2024'te çıkış sayısı 422'ye düşmüş. Kalıcı olduğu kesin değil.
- 7.000 oyuncuyla yapılan ankette oyuncuların **%52'si**, üst üste rahatsız edici reklam görürse oyunu bırakacağını söylüyor. ([Deloitte + Google AdMob, 2025](https://www.deloitte.com/us/en/industries/tmt/articles/improve-mobile-game-advertising.html))
- Mağaza yorumlarına göre reklam kaldırma için **0,99-4,99 $** makul bulunuyor; 5 $ üstüne şikâyet geliyor. ([AppFollow](https://appfollow.io/blog/what-mobile-game-players-want-monetization-insights-from-app-store-reviews), tarihsiz)

### Sakin (cozy) oyunlar
- Steam'de "cozy" etiketli oyun sayısı: 2024'te 389, 2025'te 650, 2026'da şimdiye kadar 1.341. ([PC Gamer](https://www.pcgamer.com/games/life-sim/are-we-in-the-cozy-gaming-gold-rush-era-cozy-has-grown-over-250-percent-on-steam-and-200-percent-in-my-inbox-since-2024/))
- Bu patlama PC'de. Mobilde aynı özenle yapılmış sakin oyun sayısının daha az olduğu bir **tahmin**; ölçen bir kaynak bulamadım.

### Türkiye
- Türkiye iç pazarında mobil oyun geliri 2025'te **%6 artarak 347 milyon $** oldu. ([gamedev.net / AppMagic](https://gamedev.net/news/turkiyes-domestic-mobile-revenue-grew-6-to-347m-in-2025-r3836/))
- En çok indirilen tür hyper casual (**%28,6**). Ortalama oyun oturumu 32,8 dakikayla dünya ortalamasının üstünde. ([CNBC-e](https://www.cnbce.com/teknoloji/turk-oyuncular-dunyayi-gecti-mobil-oyunlarda-en-uzun-oturum-suresi-h17731))
- Kelime oyunları: Kelimelik 25 milyon üye diyor (mağaza sayfasındaki kendi iddiası) ve çevrim içi rekabet oyunu. Wordle Türkçe büyük ölçüde web'de oynanıyor. Çengel bulmaca ve kelime gezmece tarzında yeni ve küçük uygulamalar var. ([App Store: Kelimelik](https://apps.apple.com/ms/app/kelimelik/id563803371), [ensonhaber](https://www.ensonhaber.com/oyunlar/wordle-turkce), [tamindir](https://www.tamindir.com/blog/android-icin-en-iyi-kelime-oyunlari_15673/))

### AKK PLAY STUDİO için fırsatlar
1. **Günlük Türkçe kelime bulmacası** (internetsiz, sakin, az reklam). Rakip var ama "günde bir bulmaca + seri (streak) + özenli tasarım" boşluğu görünüyor (tahmin).
2. **Mobil için sakin yerleştirme / düzenleme bulmacası** (PC'deki cozy patlamasının mobile taşınması, tahmin).
3. **KIVILCIM'i büyütmek:** aynı tarz, düşük risk. Yeni oyun değil ama aynı kitleye gider.

**Bulamadıklarım:** "Mobilde şu tür eksik" diyen güvenilir bir ölçüm yok. Bu tür iddialar çoğunlukla kaynağı belirsiz sitelerden geliyor; bunları kullanmadım.

---

## 2. Kaan: önerilen oyun fikirleri

| | Fikir | Tek cümle | Yapım zorluğu |
|---|---|---|---|
| **Önerilen** | **Günlük Kelime** | Her gün herkese aynı Türkçe kelime bulmacası; çöz, serini koru, sonucunu kelimeyi ele vermeyen renkli karelerle paylaş. | Düşük |
| 2 | **Yerli Yerine** | Dağınık bir çarşı tezgâhını, dede evinin dolabını eşyaları doğru yere yerleştirerek topladığın sakin bulmaca. | Orta |
| 3 | **KIVILCIM: Günlük Işık** | KIVILCIM'e her gün yeni bir bölüm ekleyen mod. | Düşük |

**Günlük Kelime, temel döngü:** Uygulamayı aç → günün bulmacasını 2-5 dakikada çöz → serin büyüsün → yarın yeni bulmaca. Arşivde geçmiş günlerin bulmacaları (reklam izleyerek ya da tek seferlik satın almayla açılır).
**Oyuncuyu geri getiren şey:** Günlük seri ve "bugünkünü çözdün mü?" paylaşımı.
**Risk:** Kelime listesi. TDK sözlüğünü izinsiz kullanmak yasal risk taşıyor; açık lisanslı bir Türkçe kelime listesi bulunmalı ya da liste elle hazırlanmalı.

---

## 3. Mert: süre ve token tahmini (Claude Code ile)

**Varsayımlar:** 1 kişi, yarı zamanlı (günde 2-3 saat). KIVILCIM'deki teknik altyapı kullanılıyor. Görsel ve ses basit tutuluyor. Rakamların tamamı **tahmin**.

| Aşama | Günlük Kelime | Yerli Yerine |
|---|---|---|
| Oynanabilir ilk sürüm (prototip) | 1-2 gün | 3-5 gün |
| Küçük ama bitmiş bir parça (dikey kesit) | 1 hafta | 2-3 hafta |
| İçerik (kelimeler / bölümler) | 1 hafta (ağırlıklı insan işi) | 3-5 hafta (40+ bölüm) |
| Test + mağaza hazırlığı | 1 hafta | 1-2 hafta |
| **Toplam** | **~3-5 hafta** | **~2-3 ay** |

### Token ve para
- **Abonelikle (önerilen):** Claude Code, 5 saatlik pencere ve haftalık üst sınırla çalışıyor. Pro ayda 20 $, Max ise ayda 100 $'dan başlıyor ([DataCamp](https://www.datacamp.com/tutorial/claude-code-usage-limits), [Anthropic yardım sayfası](https://support.claude.com/en/articles/15910845-claude-code-may-july-2026-weekly-limits-promotion)).
  - Günlük Kelime: **Max 5x ile 1 ay (~100 $)**. Pro ile de olur, ama sık sık limite takılırsın.
  - Yerli Yerine: **Max 5x ile 2-3 ay (~200-300 $)**.
- **API ile ödenirse (karşılaştırma için):** Günlük Kelime ~150-500 $, Yerli Yerine ~500-2.000 $ (tahmin). Günde 3-5 saat kullanan biri için abonelik, API'ye göre yaklaşık 2-2,5 kat ucuz çıkıyor ([DEV Community](https://dev.to/yurukusa/the-token-per-dollar-math-running-claude-max-for-30-days-2k1o)).
- **Gerçek örnekler (ölçek fikri versin diye):**
  - Tek seferde yapılan bir tarayıcı oyunu: 8 saat, ~445 milyon girdi tokeni, API fiyatıyla ~550 $ ([The New Stack](https://thenewstack.io/claude-fable-game-demos/)). Bu, ajanın hiç durmadan çalıştığı uç bir örnek. Etkileşimli çalışma çok daha az token harcar.
  - Bir mobil kule savunma oyunu: ~20 saatte 42.000 satır kod ve 589 test ([dev günlüğü](https://cxyda.github.io/ProjectAegisDevLog)).
  - Bir maliyet örneğinde ilk prototip turu 114 $ tuttu, dokuzuncu turda 30 $'a düştü: proje oturdukça maliyet azalıyor ([agentconn](https://agentconn.com/blog/fable-5-receipts-ported-game-50m-lines-149-invoice-ai-coding-2026/)).

### Riskler
| Risk | Olasılık | Etki | Önlem |
|---|---|---|---|
| Kelime listesinde lisans sorunu | Orta | Yüksek | Açık lisanslı liste kullan; yoksa listeyi kendin hazırla |
| İçerik üretimi beklenenden uzun sürer | Yüksek | Orta | İlk sürümü 60 günlük bulmacayla çıkar |
| Limite takılıp beklemek | Orta | Düşük | Max 5x'e geç; uzun işleri mesai dışına koy |
| Mağazada görünmemek | Yüksek | Yüksek | KIVILCIM sayfasından çapraz tanıtım; Türkçe arama kelimeleri |

## Onay gerekiyor
- [ ] Hangi fikirle ilerlenecek?
- [ ] Abonelik seçimi (Pro mu, Max 5x mi)
- [ ] Kesin karar öncesi AppMagic / Sensor Tower'dan Türkiye kelime oyunu indirme verisine bakılsın mı?
