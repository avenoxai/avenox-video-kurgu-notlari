# Pahalıya patlayan dersler

## Beş ders

1. **Daha çok ajan daha hızlı demek değil.** Ajanları çok paralelleştirince problem çıkar: limitlere takılır, işler yarıda kesilir, ajan "bitti" der ama bitmemiştir. Çözüm protokol: protokol doğrudan dosyaya bakar; ajan dediği işi dosyaya yazmadıysa iş bitti sayılmaz.
2. **Aynı hatayı birden fazla görüyorsan orada problem var: koda yaz.** Skill olarak değil, model doğru yapmadığı sürece geçemeyeceği bir sistem olarak (`04-kapilar.md`).
3. **Eşikleri kendin koy.** Hız, hareket yoğunluğu, renk, süre: modelin tahmin etmesini bekleme, sayıyla ver.
4. **Detayları standart haline getir.** Modelin senin istediğin tarzı anlaması için tarzın yazılı bir standarda dönmeli. Instagram'ı kaydırınca hepsi birbirinin aynısı, çünkü bu kısımla uğraşılmıyor.
5. **Ne transkripte ne ajanın raporuna körü körüne güven.** Son söz sende. İzle, incele, hoşuna gitmediyse ajana söyle: şu değişecek, şu olacak.

## Arıza kataloğu

| Arıza | Ne oldu | Bugünkü önlem |
|---|---|---|
| Ses ve görüntü kayması | İlk denemelerde uzun videolarda ses ile görüntü kaydı | Özel motor: senkron tutmuyorsa birleştirmeyi reddeder |
| Limit ve yarıda kalan işler | Çok sayıda ajan açınca limitlere takıldı, işler yarıda kesildi | Tek şef, dosya sözleşmesi, render kuyruğu, limite göre detay ayarı |
| Sahte "bitti" | Ajan bitti dedi, iş bitmemişti | Teslim formu yoksa bitmemiş sayılır |
| Tek bağlantı hatası | Büyük kurguda bir hata bütün ajanları düşürebilir | Dosyada tutulan durum, kaldığı yerden devam |
| Farklı göz rengi | Göz satırı yokken görsellerin yarısına yakını farklı göz rengiyle çıktı | Promptta göz için renk kodu |
| Bacak yerine boru | Kapakta karakteri her seferinde yeniden çizdirince altına sarı boru geldi | Onaylı pozlar, kapak kodla kuruluyor |
| Beyaz ekran | İlk editlerde ekran neredeyse beyazdı, göz yordu | Sıcak kraft zemin, telefonda ışık ölçümü |
| Yavaş kurgu | "Bir hareket bitmeden yenisi başlamasın" kuralı videoyu yavaşlattı | 10 saniyede ortalama 10-10,5 hareket hedefi |
| Çelişkili prompt | "Bacak ekleme" denmişti ama iki referansta da bacak vardı | Ajan çelişkiyi söyledi, sahneyi masada kurguladı; kısıtları referanslarla karşılaştır |

## Değişecek, mantık kalacak

Modeller değişiyor, yöntemler değişiyor, sürecin kendisi değişiyor. Bu notlardaki araç ve sürüm adları zamanla
eskiyecek. Kalacak olan arkadaki mantık: tek şef, dosyada sözleşme, ölçülebilir çıta, koda yazılan hata, kilitli marka,
son sözün sende olması.
