# GitHub'a yükleme ve GitHub Pages kurulumu

## 1 — Dosyaları yükle

1. `LexHukuk-GitHub-Pages.zip` arşivini bilgisayarına indir.
2. Dosyaya sağ tıkla → **Tümünü Ayıkla**.
3. Tarayıcıda https://github.com/KadirGurlu/LexHukuk adresine git.
4. `Add file` → `Upload files` seç. Ekranda Add file yoksa `+` menüsünden dosya ekleme seçeneğini aç.
5. Çıkardığın `index.html`, `assets/`, `data/`, `docs/`, `.nojekyll` ve `README.md` dosyalarını (arşivi değil) yükle. GitHub tarayıcı arayüzü klasör sürükle-bırak da kabul eder.
6. `Commit changes` ile `main` dalına kaydet. Mevcut `README.md` için üzerine yazma uyarısı gelirse bu paketin README dosyasını tutabilirsin.
7. Dosya ağacında `index.html` ve `assets` klasörünü gördüğünü kontrol et.

> Windows varsayılan ayarlarda `.nojekyll` dosyası gizli görünebilir. GitHub Pages için bu projede zorunlu değil; yüklemezsen de site çoğunlukla çalışır.

## 2 — GitHub Pages ile yayınla

1. Depoda `Settings` sekmesini aç.
2. Soldan `Pages` menüsüne gir.
3. `Build and deployment` alanındaki `Source` seçeneğini `Deploy from a branch` olarak ayarla.
4. `Branch`: `main`, dizin: `/(root)` seç.
5. `Save` düğmesine bas.
6. Yayın tamamlandığında GitHub Pages bölümünde site adresin görünür:
   https://kadirgurlu.github.io/LexHukuk/

**Önemli:** GitHub Free hesabıyla Pages özelliği public depolarda kullanılabilir. Eğer depo private ise ve Pages izin vermiyorsa, `Settings → General → Danger Zone → Change repository visibility` üzerinden depoyu public yapman gerekir. Bu durumda kodun herkesçe görülebilir olur. Private repo üzerinden GitHub Pages, uygun ücretli GitHub planlarında desteklenir; yayındaki site erişimi ayrıca herkese açık olabilir.

## 3 — Site çalışmıyorsa

- `index.html` ana dizinde mi? (`LexHukuk-GitHub-Pages/index.html` gibi fazladan klasör düzeyi olmamalı.)
- `assets/app.js`, `assets/style.css`, `assets/terms.js` aynı klasörde mi?
- Repo ve Pages şubesinde `main` seçili mi?
- Bilgisayarda dosyaları doğrudan `index.html` açarak görebilirsin; sayfanın işlevleri için JS etkin olmalı.

## 4 — Yeni kelime ekleme

Sitedeki `Yerel Editör` ekranından CSV içe aktarabilir ve mevcut veri setini JSON olarak indirebilirsin. Bu değişiklikler yalnızca kendi tarayıcında saklanır; diğer ziyaretçiler görmez.

Herkesin göreceği kalıcı kelimeleri eklemek için `data/build_data.py` içindeki `raw` verisini güncelleyip `python data/build_data.py` çalıştır; oluşan `assets/terms.js` dosyasını GitHub'a tekrar yükle.

## Teknik sınırlar

GitHub Pages sadece statik site barındırır. Güvenli şifreli hesaplar, Google ile giriş, birden çok cihaz arasında senkronize ilerleme ve korumalı yönetim paneli bu sürümde bulunmaz. Bunlar için bağımsız bir backend/veritabanı kurulmalıdır.
