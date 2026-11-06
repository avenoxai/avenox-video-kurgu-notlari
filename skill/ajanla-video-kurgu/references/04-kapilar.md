# Kapılar: hatayı nota değil koda yaz

Kapı, bir işin geçmesini engelleyen şey. Kapı fikri de Sirio'nun sisteminden; kendi kurallarına göre değiştir.

## Kural

> Bir hatayı iki kere yapıyorsak onu nota değil direkt koda yazıyoruz.

Not (skill, talimat) modelin hatırlamasına bağlıdır; model bazen unutur. Kod ise çalışır: kontrol geçmezse
video çıkmaz, model işi tekrar yapmak zorunda kalır. Bu kuralı ana ajana bir kez söyle, kendi skill'ine eklesin;
sonraki her tekrar eden hata otomatik olarak kapıya dönüşür.

## Kapı nasıl yazılır

1. Hatayı ölçülebilir hale getir: "kayıyor" değil, "ses ile görüntü arasındaki fark 1 kareyi geçiyor" (örnek eşik, videoda yok).
2. Kontrolü kod olarak yaz (betik, test, render öncesi doğrulama). Kodu ajan yazabilir: "videolarımda ses kayması olmasın, bunun için bir sistem yaz" demek yeter.
3. Kapıyı istasyonun çıkışına koy. Geçmezse iş geri döner, gerekçesiyle.
4. Kapının ne zaman eklendiğini ve hangi hatadan doğduğunu bir satır not et.

## Örnek kapılar

| Hata | Kapı |
|---|---|
| Uzun videolarda ses ve görüntü kayıyor (kısa Reels'ta sorun olmaz, uzunda her zaman kayar) | Birleştirmeden önce senkron kontrolü; tutmuyorsa motor birleştirmeyi reddeder |
| Ajan "bitti" diyor, bitmemiş | Teslim formu dosyası yoksa ya da eksikse iş bitmemiş sayılır |
| Karakterin gözleri bozuk çıkıyor | Promptta göz için renk kodu; her üretimden sonra yüz kırpımının kimlik görseliyle karşılaştırılması (öneri, videoda yok) |
| Kurgu çok yavaş ya da çok hızlı | Hareket yoğunluğu ölçümü: 10 saniyedeki ortalama hareket sayısı hedef aralıkta mı (videodaki ayar: 8'den 10-10,5'e çıkarıldı) |
| Ekranda yasaklı stil (neon, mor gradyan, parlama, emoji) | Yasak listesi kontrolü |
| Kapakta Türkçe harf hatası (büyük İ gibi) | Kapak yazısını model çizmez, kod dizer |

## Ölçerek düzelt

"Bir tık yavaş kalmış" dendiğinde ajan baktı, ölçtü: 10 saniyede ortalama 8 hareket varmış. Hedef 10-10,5 olarak
kondu ve artık bu standart takip ediliyor. Önceki bir ayar ("bir hareket bitmeden yenisi başlamasın") videoyu fazla
yavaşlatmıştı; kelimeyle verilen kural yanlış yere gitti, sayıyla verilen hedef tuttu.

Eşikleri kendin koy. Model senin istediğin tarzı tahmin edemez; standardı sen belirlersin, dosyaya yazarsın.
