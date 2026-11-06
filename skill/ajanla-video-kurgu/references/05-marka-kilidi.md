# Marka kilidi

Ajanlar her oturuma sıfırdan başlar ve ortalamayı yapar. Problem tam olarak ortalama iş çıkarmasından doğar.
Kalıcı marka değerlerini skill ya da marka dosyası olarak tutmazsan slop'tan kurtulamazsın.

## Marka dosyasında ne olur

- **Karakter / maskot / ürün:** tek cümlelik tanım + kimlik görseli + oran (karakter) sayfası
- **Renkler:** hex kodlarıyla (tarif değil, sayı)
- **Zemin ve tarz:** ör. sıcak kraft zemin, grain dokusu
- **Yazı:** kapak ve ekran yazısı kuralları (kelime sınırı, font)
- **Yasaklar:** ne asla olmaz
- **Beğenmeme defteri:** kullanıcının beğenmediği her şey, tarihiyle (`../templates/begenmeme-defteri.md`)

## Karakteri kilitle

Gözü bozuk ya da şişkin bir karakter videoyu ucuz yapay zeka işine çevirir. Bu yüzden kimlik tartışılmaz olur:

- Her işe **aynı iki görsel** verilir: kimlik görseli ve farklı açılardan oran sayfası (karakter sheet).
- Karakter insan, maskot ya da gerçek bir ürün olabilir; görsel modelden karakter sheet oluşturmasını istersen yapar. Önce bunu kilitle.
- Ajan asla yapmaması gerekenleri bilir: ör. karakteri şişmanlatmamak, el parmak sayısına dikkat.
- En çok bozulan kısım gözler. Göz akının rengini artık sayıyla ver: promptta tek bir satır, içinde rengin kodu. Bu satır yokken görsellerin yarısına yakını farklı göz rengiyle çıkmış, hepsi çöpe gitmişti. Tarifin yanında sayı verdiğinde görsel modeller bu işi çok iyi yapar.

## Sakin karakter akılda kalır

Görsel modeller karakterleri parlak ve abartılı çizmeyi sever; dikkat çeksin ister. Sonuç slop gibi durur.
Videodaki maskot uzun, ince, ifadesiz bir limon: şişman değil, bağırmıyor, garip tepki vermiyor.
Modellerin kendiliğinden yapmadığı şey olduğu için akılda kalıyor. Kendi markanda da modelin varsayılanına karşı bir seçim yap.

## Renkleri ölç

İlk editlerde ekran neredeyse beyazdı ve göz yoruyordu. Sıcak kraft zemine geçildi; telefonda ölçünce ekrandan gelen
ışığın neredeyse yarı yarıya azaldığı görüldü. Gece izleyen biri için fark büyük. Renk kararlarını göz kararı değil, ölçerek ver.

## Yasak listesi

Videodaki liste: neon yok, mor gradyan yok, parlama efekti yok, emoji yok. Bunlar işi ucuz gösteriyor.
"Daha iyi yap" demek bir şey ifade etmez; neyi istemediğini net yazarsan model uygular.

## Kapak ve başlık (videoda: Instagram / kısa form kapakları)

- Kapakları model her seferinde baştan çizmez. Karakteri her seferinde yeniden çizdirince bir gün altına bacak yerine sarı bir boru koydu, garip hareketler yaptı.
- Çözüm: onaylı pozları başta bir kez üret, kapağı **kodla** kur (poz + yazı). Türkçe büyük İ gibi harfler bu sayede hep doğru çıkar.
- Kısa form kapak kuralı (videodaki): en fazla 4 kelime, büyük karakter, tek bir jest.
- Başlık abartmaz: videoda ne varsa onu söyler.

## Logolar

Bir ürünün adı geçiyorsa resmi logosu gelir. Logoyu modele çizdirme, yeniden çizme, uydurma.

## Beğenmeme defteri

Ajana şu görevi ver: kullanıcı bir şeyi beğenmediğinde o an dosyaya tarihiyle yazsın.
"Şu tarihte X şunu beğenmedi ve bunu söyledi." Sistem bu deftere göre düzenli olarak gelişir;
aynı düzeltme ikinci kez gelirse kapıya döner (`04-kapilar.md`).
