# ÉLAN — 3D Parfüm Konsept Prototipi

Three.js ile hazırlanmış, etkileşimli bir 3D parfüm e-ticaret vitrini.

**Canlı:** https://aniloz.dev/elan-parfum/

> ÉLAN gerçek bir marka değildir. Bu site bir **konsept prototiptir**; satış yapılmaz, ürünler ve fiyatlar örnektir.

## Özellikler
- Markalı giriş ekranı (perde açılış animasyonu)
- Havada süzülen, yay fiziğiyle hareket eden ve kendi ekseninde dönen 3 şişe (karusel)
- Şişeye tıklayınca kapak açılır, sprey sıkılır (parçacık sisi), şişe büyüyüp sola geçer
- 4 bilgi sekmesi (Üst / Kalp / Alt notalar, Şişe & Detay): kamera şişenin ilgili kısmına yaklaşır, bilgi 3D model üzerinde etiketlenir
- Şişenin bir bölümüne tıklayarak da sekme seçilebilir, sürükleyerek döndürülebilir
- **Koku yolculuğu grafiği:** üst / kalp / alt notaların zamana yayılışı; grafikte gezinince şişenin ilgili kısmı parlar, tıklayınca o bölüme gidilir. Altında akor dağılımı
- **Kişiye özel gravür:** yazılan isim etikete canlı olarak işlenir (el yazısı / büyük harf), fiyat güncellenir
- **Ses tasarımı:** sprey, cam kapak, geçiş ve arayüz sesleri ile parfüme göre değişen ambiyans; hepsi Web Audio ile kodla sentezlenir (ses dosyası yok), sağ üstten kapatılabilir
- Çalkalanan sıvı (şişenin hareketine tepki veren yüzey), bulanık yansımalı zemin, yumuşak gerçek zamanlı gölgeler
- Post-processing: bloom, kromatik sapma, vinyet, film greni; düşük kare hızında kalite otomatik düşer
- Detay sayfasında parfümler arası geçiş (oklar / klavye)
- Mobil uyumlu

## Doğrudan bağlantılar
- `?p=2` — 2. parfümle başla
- `?p=3&d=1` — 3. parfümün detayını aç
- `?p=1&d=1&t=heart` — detayda bir sekmeyi aç (`top`, `heart`, `base`, `detail`)
- `?skip=1` — giriş ekranını atla

## Künye
- **Fikir, tasarım ve yönlendirme:** Anıl — [aniloz.dev](https://aniloz.dev)
- **Yapay zekâ desteği:**
  - Kod ve 3D sahne: Claude Code (Anthropic)
  - Arka plan ve stüdyo ortam görselleri: Antigravity (Google)
  - Etiket ve giriş ekranı dokuları: Codex (OpenAI)

## Teknoloji
Three.js · WebGL · GSAP · Web Audio — derleme adımı yok, tek `index.html`.

Yol haritası için [ROADMAP.md](ROADMAP.md).

## Yerelde çalıştırma
```bash
python3 -m http.server 5173
```
Ardından http://localhost:5173 adresini aç. (`?skip=1` giriş ekranını atlar.)
