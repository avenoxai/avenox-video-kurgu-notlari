# Atölye: üç hat, sekiz istasyon

Aynı atölyeden üç farklı video çıkar. Malzemeye göre hat seç.

| Hat | Elindeki | Ajanın işi |
|---|---|---|
| **Yalnız ses** | Ses kaydı (notlara bakarak doğaçlama ya da metin) | Her kareyi kodla üretir: ses kaydına uyan motion video, özel görsel ve kliplerle desteklenmiş |
| **Ekran kaydı** | Ekranda gösterip anlattığın kayıt | Kesime dokunmadan üstüne grafik, zoom, efekt bindirir; özel bilgileri bulanıklaştırır |
| **Kısa form** | Biten uzun video | Kesit çıkarır, kontrol eder, takvime dağıtır; ya da sahneyi baştan dikey kurar |

Ekran kaydında ajana genel bir tarif yeter: "Şu sahnelere dikkat et, bunları kullanmak istiyoruz, özel bilgilerimi sansürle."
Yalnız seste sadece "bunu motion video yap" demek slop üretir: herkes böyle yapıyor. Fark, aşağıdaki düzende.

## İstasyonlar

Her istasyonun çıkışında bir kapı var. Kapı geçmeden iş sonraki istasyona gitmez.

| # | İstasyon | Girdi | Çıktı (dosya) | Kapı |
|---|---|---|---|---|
| 1 | Kayıt ve ses | Ham kayıt | İşlenmiş ses (aynı uzunlukta, aynı hizada) | Yayın seviyesinde mi (ör. -14 LUFS), tepe sınırın altında mı |
| 2 | Transkript | Ses | Zaman kodlu metin | Temizlik ajanı adları düzeltti mi (ör. "Claude" ile "cloud") |
| 3 | Kesim | Ses + metin | Kesim listesi + kesilmiş kayıt | Kesilen yerler dinlenip okundu mu, yarım kelime kaldı mı |
| 4 | Pano haritası | Kesilmiş metin | Pasaj pasaj harita | Her pasajda "sadece dinleyen anlar mı?" cevabı var mı |
| 5 | Bölüm brief'leri | Harita + marka dosyası | Bölüm başına brief | Brief'te değişmeyecek kararlar, çıta, boş bırakılanlar yazıyor mu |
| 6 | Üretim | Brief'teki görsel/video ihtiyacı | Etiketli görsel ve klipler (kütüphanede) | Karakter kimlik görseliyle yan yana aynı mı |
| 7 | Paralel kurulum | Brief'ler + kütüphane | Bölüm kodu + teslim formu | Teslim formu dolu mu, bölüm kendi kapılarından geçti mi |
| 8 | Render ve yayın | Bölümler | Final video, altyazı, kapak, kısa form | Ses-görüntü senkronu, süre, ses seviyesi, son izleme |

Kaydı sen alırsın; sonraki istasyonların neredeyse hepsinde bir ajan çalışır, bir başkası onu kontrol eder.

## Sırayla neden?

Uzun bir video, aynı anda çok ajan. Plan yoksa bunların beraber çalışma ihtimali yok.
Bu yüzden önce kesim ve harita, sonra paralel iş: plan baştan düzgün olunca orkestrasyonda problem çıkmaz.

- Ham kaydın yarısından fazlası boşluk çıkabilir; önce onu kes.
- Kesim bittikten sonra ajanlar kesime dokunmaz, üstüne bindirir.
- Görsel ve video ihtiyacı haritadan çıkar, rastgele değil.

## Bitmiş bir videodan sayılar (örnek, hedef değil)

- 95 dakikalık çekim, 30 dakikaya kesildi; üstüne yüzlerce özel görsel ve efekt.
- Normal bir videoda yaklaşık 150 özel görsel, 10-15 ya da daha fazla özel klip.
- Yalnız ses kaydı verilen bir video 1,5 saatte yüklemeye hazır oldu.
- Gece bırakılan edit sabah bitmişti.
- Promptların yarısı tek satırı geçmiyor, çünkü uzun protokolü ana ajan yazıyor.
