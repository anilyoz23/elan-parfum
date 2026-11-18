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
- Mobil uyumlu

## Künye
- **Fikir, tasarım ve yönlendirme:** Anıl — [aniloz.dev](https://aniloz.dev)
- **Yapay zekâ desteği:**
  - Kod ve 3D sahne: Claude Code (Anthropic)
  - Arka plan ve stüdyo ortam görselleri: Antigravity (Google)
  - Etiket ve giriş ekranı dokuları: Codex (OpenAI)

## Teknoloji
Three.js · WebGL · GSAP — derleme adımı yok, tek `index.html`.

## Yerelde çalıştırma
```bash
python3 -m http.server 5173
```
Ardından http://localhost:5173 adresini aç. (`?skip=1` giriş ekranını atlar.)
