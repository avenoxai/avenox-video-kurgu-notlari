# Pano haritası

Fikir Sirio'nun açık kaynak kurgu sisteminden: https://github.com/sirioberati/YouTube-AI-Video-Editing-System
Kendi hattına göre uyarla; fikir onun.

## Ne zaman

Kesim bittikten sonra, grafiğe geçmeden önce. Harita olmadan bölümleri ayrı ajanlara dağıtmak,
birbirinden kopuk bölümler demek.

## Nasıl

Ana ajan kesilmiş metni baştan sona okur ve her pasaj (sahne) için tek bir soru sorar:

> Bunu sadece dinleyen izleyici anlar mı?

- **Anlıyorsa:** ekrana ek metin koyma. Görüntü sesi tekrar etmez; atmosfer, hareket, karakter yeter.
- **Anlamıyorsa:** ne gösterileceğini yaz: hangi logo, hangi kaynak (makale, sayfa, belge), hangi rakam, hangi arayüz.

Gerçekte pasajlar dakikalık değil, çok daha sık bölünür. 10 dakikalık bir video 10 parça değil, onlarca sahnedir.

## Neden

Grafikleri bölüm bölüm ayrı ajanlar kurar. 30 dakikalık bir videonun editini tek ajana bırakırsan günler sürebilir;
aynı anda 10 ajan çalıştırırsan her biri kendi parçasını alır. Bunu mümkün kılan şey harita: her ajan neyi göstermesi
gerektiğini, önceki ve sonraki sahnenin ne olduğunu dosyadan okur.

## Çıktı

Şablon: `../templates/pano-haritasi.md`. Her satırda:

- zaman aralığı ve konuşulan cümleler (transkriptten, birebir)
- "dinleyen anlar mı?" cevabı
- ekranda ne olmalı (logo, kaynak kartı, rakam, arayüz, karakter eylemi)
- gereken özel görsel / klip (varsa) ve kütüphanede karşılığı olup olmadığı
- önceki ve sonraki sahneyle geçiş notu

Logo kuralı: bir ürünün adı geçiyorsa resmi logosu gelir, yalnız metin ya da uydurma işaret değil.
Kaynak kuralı: alıntı varsa kaynağın kendisi ekrana gelir, alıntı birebir olur, kaynağı açılıp doğrulanamayan şey alıntı olarak gösterilmez.
