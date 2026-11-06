# Orkestrasyon: tek şef, dosyalar, teslim

Ajan eklemek kolay. Zor olan, birbirinin işini bozmadan beraber çalıştırmak.
Büyük bir ajan orkestrasyonu kurmak şart değil: ana ajanın kendi iş akışı (ör. Claude Code'da workflow / ultracode) yeter.
Şart olan, aşağıdaki sözleşmenin dosyalarda durması.

## Tek şef

- Kullanıcı tek bir ana ajanla konuşur (ör. tek bir Claude Code oturumu). Diğer ajanlar onun altında çalışır.
- Ana ajan kullanıcının niyetini anlar, planı yazar, işi bölümlere böler, alt ajanlara dağıtır, teslimleri kontrol eder.
- Uzun protokolü kullanıcı yazmaz, ana ajan yazar. Kullanıcının promptu tek satır olabilir; ana ajan onu ölçülebilir bir sözleşmeye çevirir.

Gerçek bir örnek (kullanıcının yazdığı tam prompt): "Editini yap. Ses efekti. Motion. Birkaç sahneye animasyon. Aşırı abartma. Acelem var. Paralel paralel çıkart."
45 dakika sürmeden ikinci sürüm bitti, çünkü uzun protokolü ana ajan yazdı.

## Dosya sözleşmesi

Ajanlar birbiriyle konuşmaz; çok ajan birbiriyle konuşunca problem çıkar. Her şey dosyada:

| Dosya | Kim yazar | İçinde |
|---|---|---|
| Transkript | İstasyon ajanı üretir, ana ajan kontrol edip ortak klasöre koyar | Zaman kodlu, temizlenmiş metin |
| Kesim listesi | İstasyon ajanı üretir, ana ajan kontrol edip ortak klasöre koyar | Nereler kesildi, neden |
| Pano haritası | Ana ajan | Pasaj pasaj ekranda ne olacak |
| Bölüm brief'i | Ana ajan | Her bölümün mantığı, önceki/sonraki sahne, çıta |
| Teslim formu | Alt ajan | Ne yapıldı, hangi varlıklar kullanıldı, hangi kapılar geçti, açık kalan ne |
| Marka dosyası | Kullanıcı + ana ajan | Değişmez marka kararları |

Ortak dosyaları **her zaman ana ajan** yazar. Alt ajan yalnız kendi bölümünü kurar ve kendi teslim formunu yazar.

## Alt ajana ne verilir

Çok fazla detay değil. Üç şey:

1. **Değişmeyecek kararlar:** marka, karakter, renkler, zemin, yasaklar, bölümün süresi ve sınırları
2. **Kalite çıtası:** ör. "hiçbir kare sıradan bir web sayfası gibi görünmesin", "10 saniyede ortalama 10-10,5 hareket"
3. **Bilerek boş bırakılan kısımlar:** tarifi ona bırakılan yerler

Çıtayı yaz, detaylı tarifi ajana bırak. Detaya girdikçe kalite düşer. Ama bir şeyi sayıyla verebiliyorsan ver.
Şablon: `../templates/bolum-brief.md`.

## Teslim formu ve "bitti" tanımı

- Alt ajan işini bitirince yaptığının tamamını teslim formuna yazar (`../templates/teslim-formu.md`).
- **Form yoksa iş bitmemiş sayılır.** Ajan "bitti" der, bakarsın bitmemiş: bu en sık arıza. Ana ajan dosyaya bakar, söze değil.
- Ana ajan teslimleri sürekli kontrol eder; eksik olanı geri gönderir.

## Kaldığı yerden devam

Büyük kurgularda tek bir bağlantı hatası çalışan bütün ajanları düşürebilir. Bu yüzden her alt ajan ilerlemesini adım adım
kendi teslim formuna yazar. Ajan düşerse yenisi önce o formu okur, işaretli adımları tekrar etmez; baştan başlamaz.

## Render kuyruğu

Paralel çalışmak işi gerçekten hızlandırır (acil bir videoda çok sayıda paralel ajanla ana iş 15 dakikada bitti).
Ama her ajan kendi kodunu yazıp kendi videosunu render etmeye kalkarsa birbirlerini patlatırlar.

- Kod ve görselleştirme paralel yazılır.
- **Render tek sırada alınır**, ayrı bir alan olarak. Alt ajan render komutunu çalıştırmaz; teslim formuna "render hazır" yazar. Ana ajan bölümleri sırayla render eder (aynı anda tek render süreci).

## Limit ayarı

Bu iş ucuz değil, limit yer. Detay seviyesini bütçeye göre ana ajana söyle:

- Limit bolsa: "sayıları artır, kurgudaki detayı artır" (daha çok hareket, daha çok özel animasyon).
- Limit azsa ve hızlı çıkması gerekiyorsa: daha az hareket, daha az özel animasyon.

## Prompt sözleşmesi

Her görev, kısa ya da uzun, dört parçadan oluşur. Şablon: `../templates/prompt-sozlesmesi.md`.

1. **Hedef:** tam olarak ne istediğin.
2. **Kısıt:** neyi asla istemediğin.
3. **Kalite çıtası:** ne olursa "iyi" diyeceğin, mümkünse ölçülebilir.
4. **Örnek:** referans görsel, beğendiğin eski iş.

Araya **kontrol noktası** koy (ör. önce storyboard, onay gelmeden üretim yok).

Videodaki örnek, 15 saniyelik karakter filmi:

- Hedef: karakter kayıt masasından kalkar, kesim masasına gider, yayın düğmesine basar.
- Kısıt: gözler, oran ve renkler birebir kalsın; bacak ekleme; başka bir şey ekleme.
- Çıta: her karedeki karakter, kimlik görseliyle yan yana konunca aynı karakter gibi görünmeli.
- Örnek: iki görsel (kimlik ve oranlar).
- Kontrol noktası: önce iki farklı yön ve seçilen yön için 3 sahnelik storyboard öner, onayı bekle.

Ajan çelişkiyi yakalayabilir: "bacak ekleme" denmiş ama iki referansta da bacak var. İyi ajan bunu söyler ve
çözüm önerir (sahneyi masada kurgulamak). Bu yüzden çıtayı ve kısıtı açık yazmak işe yarar.

Aynı mantık her yerde geçer:

- E-ticaret ürün videosu: "güzel bir video yap" deme. Süreyi, ürünü, asla gösterilmeyecek şeyi, beğendiğin eski bir videoyu ver.
- Yazılım: "testleri geçir" deme. Ajan bazen kodu düzeltmek yerine testi uydurur; neyin asla yapılmayacağını yaz.
