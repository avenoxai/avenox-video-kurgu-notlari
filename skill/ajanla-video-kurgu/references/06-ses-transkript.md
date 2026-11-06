# Ses, transkript ve kesim

## Ses: ne kadar az işlenirse o kadar iyi

Sesle çok oynarsan izleyici sesin yapay zekayla üretildiğini düşünmeye başlar. Çok işleme.

Ajan farklı gürültü temizleme ayarları denesin, sen o video için hoşuna gideni seç. Videoda söz verdiğim kendi zincirim (videoda ayrıntısı söylenmedi; kendi mikrofonuna göre ayarla):

1. Gürültü temizleme (DPDFNet, en çok 30 dB bastırma)
2. 80 Hz alt kesim
3. Mikrofona göre EQ
4. De-esser
5. Kompresör (3:1)
6. Konuşma -14 LUFS (yayın seviyesi), tepe -1 dBFS

Zincirin çıktısı girdiyle aynı uzunlukta ve hizada olmalı ki videoya doğrudan otursun.

Müzik: olabildiğince kısık. İzleyici hissetsin ama fark etmesin; yüksek müzik yorar.
Ses efekti ve müzik için lisanslı bir kütüphane kullan (videoda Epidemic Sound).

## Transkript: modeller sesi duyamaz

Metne dönmeyen kaydı ajanlar kullanamaz. Kurgu, görsellerin doğru anda gelmesi ve altyazı hep metinden çıkar.

- **Whisper**, açık kaynak bir model. Yerelde çalıştır: ses dışarı çıkmaz, ek ücret ödemezsin. Videodaki bilgisayarda 15 dakikalık kayıt yaklaşık 1 dakikada çıktı.
- Yerelde çalıştıramıyorsan API'lerden kullanabilirsin; önemli olan modelin adı.
- Ajana "Whisper'ı indir" demen ve ses dosyasını vermen yeter, gerisini kurar.

## Temizlik ajanı

Whisper bazı adları karıştırır (ör. "Claude" deyince "cloud" yazar: bulut ile model). En sonda bir ajan metni
temize geçirir. Kendi sık geçen adların için bir düzeltme sözlüğü tut; ajan her videoda ona göre düzeltsin.

## Kesim

1. **Boşluklar:** ekran kaydında düşünürken oluşan sessizlikleri ajan keser ("boşlukları kes" demek yeter).
2. **Tekrarlar:** aynı şeyi birkaç kez söylediğin yerleri de keser, çünkü elinde metin var.
3. **Elle son geçiş:** otomatik kesimden sonra sesi bir kez kendin düzenle.
4. Kesim bittikten sonra kurgu ajanları kesime dokunmaz; grafik, zoom ve efekt üstüne biner.

Kesimden sonra metni yeniden üret ya da zamanları kaydır: altyazı ve bölüm zamanları kesilmiş videoya göre olmalı,
ham kayda göre değil.
