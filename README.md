# LexHukuk — Almanca–Türkçe Hukuk Sözlüğü

**GitHub Pages'e doğrudan yüklenebilen, kurulum gerektirmeyen web sitesi.**

## Bu pakette ne var?

- `index.html`: web sitesinin giriş dosyası.
- `assets/style.css`: lacivert–krem responsive tasarım.
- `assets/app.js`: sözlük araması, kelime detayları, kullanıcı etkileşimleri ve çalışma modları.
- `assets/terms.js`: örnek kelime verileri (tarayıcı bu dosyayı doğrudan okur).
- `assets/favicon.svg`: site simgesi.
- `data/terms.json`: düzenlenebilir örnek veri seti.
- `data/build_data.py`: kelime dosyasını yeniden üretme betiği (opsiyonel; Python 3 gerekir).
- `.nojekyll`: GitHub Pages statik yayın ayarı.
- `docs/GITHUB-KURULUM.md`: adım adım yükleme yönergesi.

## İşlevler

- 111 örnek Almanca–Türkçe kelime, Türkçe açıklamalar ve her biri için 2 örnek cümle
- 17 hukuk alanı + genel Almanca ve 28 hazır liste
- Çift yönlü, artikelden bağımsız arama ve öneriler
- Flashcard, çoktan seçmeli test, yazma alıştırması, eşleştirme
- Favoriler, özel listeler, günlük hedef, tekrar takvimi
- İlerleme ve listelerin tarayıcıda `localStorage` içinde saklanması
- CSV/JSON içerik düzenleme ve dışa aktarma (yerel yönetim ekranı)
- Telefon, tablet ve bilgisayarda uyumlu arayüz

## GitHub'a yükleme

1. ZIP dosyasını bilgisayarınızda çıkartın.
2. [KadirGurlu/LexHukuk](https://github.com/KadirGurlu/LexHukuk) deposunu açın.
3. **Add file → Upload files** yolunu izleyin.
4. ZIP dosyasını **değil, ZIP içinden çıkan dosya ve klasörleri** yükleyin. `index.html` mutlaka deponun kökünde olmalı.
5. **Commit changes** butonuyla kaydedin.
6. GitHub Pages için `Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save` seçin.

> **Önemli:** GitHub Free hesabında GitHub Pages için depo **public** olmalıdır. GitHub Pro/Team gibi ücretli planlarda private depodan yayın mümkün olabilir. Yayınlanan Pages sitesi genel olarak internete açıktır.

Yayın adresi, Pages aktifse: `https://kadirgurlu.github.io/LexHukuk/`

Detaylı yardım: `docs/GITHUB-KURULUM.md`.

## Güvenlik ve kapsam

Bu sürüm, önceki bulut tabanlı LexHukuk uygulamasının birebir kaynak kopyası **değildir**. Önceki barındırma ortamının kaynak arşivine erişilemediğinden GitHub Pages uyumlu bağımsız bir sürüm olarak yeniden oluşturulmuştur.

Bu sürümde sunucu, veritabanı, güvenli üyelik sistemi veya gerçek rol tabanlı admin paneli **yoktur**. İçerik ekleme/düzenleme ve ilerleme verileri yalnızca **kullanıldığı tarayıcıda** saklanır. Tarayıcı verileri silinirse içerikler kaybolabilir; dışa aktarma özelliğiyle yedek alın. GitHub Pages statik barındırma sağladığından güvenli kullanıcı hesabı ve çok kullanıcılı veritabanı için ayrı backend gerekir.

Sözlük öğrenme ve prototip amaçlıdır; Alman ve Türk hukuk sistemlerindeki kavramlar her zaman birebir örtüşmez. Resmî veya akademik kaynaklarla doğrulamadan hukuki başvuru kaynağı olarak kullanmayın.
