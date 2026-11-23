# Chess Arbiter web sayfaları (GitHub Pages)

App Store Connect'te istenen gizlilik politikası ve destek adresleri için.

| Sayfa | Yayınlanınca adresi |
|---|---|
| Ana sayfa | https://arbiterchess.com/ (Türkçe: https://arbiterchess.com/tr/) |
| Gizlilik politikası | https://arbiterchess.com/privacy/ |
| Destek | https://arbiterchess.com/support/ |
| Lisanslar | https://arbiterchess.com/licenses/ |

Alan adı bağlanana kadar aynı sayfalar `https://uguraydinnn.github.io/chess-arbiter/` altında açılır; bağlandıktan sonra GitHub eski adresi yeni adrese yönlendirir. Alan adı bağlama adımları: `docs/YOL-HARITASI.md`, madde 1.3.

## İletişim

Destek e-postası: `support@arbiterchess.com` (privacy ve support sayfalarında yazılı).

## Güncelleme (23 Kasım 2026'dan beri otomatik)

Elle yükleme gerekmez. Claude siteyi üretir ve gönderir:

```
python scripts/build-site.py
python scripts/publish-site.py --dry-run   # gidecek dosyalar
python scripts/publish-site.py -m "Site: ..."
```

`publish-site.py` yalnız değişen ve yeni başvurulan dosyaları `D:\Projeler\_02-Satranç\_technical\site-yayin`
(depo kopyası) üzerinden gönderir; hiçbir dosyayı silmez, `CNAME` ve `.nojekyll` dosyalarına dokunmaz.

## İlk yayınlama (tarihçe; bir kez yapıldı)

1. github.com → sağ üstte **+** → **New repository**.
   - Repository name: `chess-arbiter`
   - **Public** seçin (ücretsiz planda Pages yalnız herkese açık depoda çalışır; uygulamanın kodu bu depoya
     girmez, yalnız bu klasördeki sayfalar).
   - **Create repository**.
2. Açılan sayfada **uploading an existing file** bağlantısına tıklayın. Bu klasörün **içindekilerin hepsini**
   sürükleyip bırakın → **Commit changes**:
   - Dosyalar: `index.html`, `style.css`, `404.html`, `robots.txt`, `sitemap.xml`, `.nojekyll`
   - Klasörler: `assets` (yazı tipleri, taşlar, simgeler), `tr` (Türkçe ana sayfa), `privacy`, `support`, `licenses`
   - `README.md` gerekmez.
   - `.nojekyll` gizli dosya olduğu için Windows'ta görünmeyebilir; zorunlu değildir.
   - **`assets` ya da `tr` eksik kalırsa** site stilsiz, yazı tipsiz ve taş görselsiz açılır, Türkçe sayfa 404 verir.
   - Depoda GitHub'ın eklediği **`CNAME`** dosyası (içinde `arbiterchess.com`) varsa **silmeyin**; özel alan adı ona bağlı.
3. Depoda **Settings → Pages** → Source: **Deploy from a branch**, Branch: **main**, klasör **/ (root)** →
   **Save**. (Depo zaten yayındaysa bu adım gerekmez.)
4. 1–2 dakika sonra yukarıdaki adresleri tarayıcıda açıp kontrol edin.

## App Store Connect (7 Kasım 2026'da girildi)

- App Privacy → **Privacy Policy URL**: `https://arbiterchess.com/privacy/`
- Sürüm sayfası → **Support URL**: `https://arbiterchess.com/support/`
- **Marketing URL**: `https://arbiterchess.com/` (Türkçe: `https://arbiterchess.com/tr/`)
