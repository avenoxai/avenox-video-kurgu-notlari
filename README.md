# Avenox: Ajanla Video Kurgu Notları

**Claude Code, Codex ya da başka bir kodlama ajanıyla uzun videoyu slop çıkarmadan editlemenin düzeni.**

Bu repo, [Claude ile Video Yapmanın Sırrı: Slop Olmayan Sistem!](https://www.youtube.com/watch?v=BAn-6Cu-cCM)
videosunda söz verdiğim skill ve notlar. Videodaki dersleri kendi ajanına verip kendi atölyeni kurman için.

Bu benim kendi kurgu hattım değil. O hat benim markam için kuruldu; kopyalarsan sana yaramaz, üstelik her yer
aynı videoyla dolar. Burada olan şey arkasındaki mantık: kim neyi yapar, iş nerede kontrol edilir,
bir hata bir daha nasıl olmaz.

---

## Nasıl kullanırsın

**1. Skill olarak kur (önerilen).** `skill/ajanla-video-kurgu` klasörünü ajanının skill klasörüne kopyala:

```bash
git clone https://github.com/avenoxai/avenox-video-kurgu-notlari.git
cp -R avenox-video-kurgu-notlari/skill/ajanla-video-kurgu ~/.claude/skills/
```

Codex ya da `SKILL.md` okuyan başka bir araç kullanıyorsan aynı klasörü onun skill dizinine koy.
Sonra ajanına "videomu editleyeceğiz, ajanla-video-kurgu skill'iyle atölyemi kur" de. İlk iş senin markanı,
malzemeni ve bütçeni soracak; cevaplarını bir dosyaya yazıp sonraki her oturumu oradan başlatacak.

**2. Notları ajanına okut.** `notlar/transkript.md` videonun tam transkripti, `notlar/bolumler.md` bölüm bölüm özet.
İlgilendiğin bölümü ajanına ver ve "bunu benim kurulumuma uyarla" de.

---

## Harita

### Skill: `skill/ajanla-video-kurgu/`

| Dosya | Ne anlatır |
|---|---|
| [SKILL.md](skill/ajanla-video-kurgu/SKILL.md) | Atölyeyi kurmanın ilk adımı, istasyonların özeti, değişmez kurallar, dört parçalı prompt |
| [01-atolye](skill/ajanla-video-kurgu/references/01-atolye.md) | Üç hat (yalnız ses, ekran kaydı, kısa form), sekiz istasyon, her istasyonun kapısı |
| [02-pano-haritasi](skill/ajanla-video-kurgu/references/02-pano-haritasi.md) | Grafiğe geçmeden önce: "sadece dinleyen anlar mı?" |
| [03-orkestrasyon](skill/ajanla-video-kurgu/references/03-orkestrasyon.md) | Tek şef, dosya sözleşmesi, alt ajana üç şey, teslim formu, render kuyruğu, prompt sözleşmesi |
| [04-kapilar](skill/ajanla-video-kurgu/references/04-kapilar.md) | Aynı hata iki kez olursa nota değil koda yaz; örnek kapılar; ölçerek düzeltmek |
| [05-marka-kilidi](skill/ajanla-video-kurgu/references/05-marka-kilidi.md) | Karakter kilidi, renk kodu, yasaklar, kapak kodla, logolar, beğenmeme defteri |
| [06-ses-transkript](skill/ajanla-video-kurgu/references/06-ses-transkript.md) | Az işlenmiş ses, ses zinciri, Whisper, temizlik ajanı, kesim |
| [07-uretim](skill/ajanla-video-kurgu/references/07-uretim.md) | Özel görsel ve video: maliyet, taslak, serpiştirme, kütüphane, model kıyası |
| [08-kisa-form](skill/ajanla-video-kurgu/references/08-kisa-form.md) | Hook, kesit hattı, takvim, tutanı genişletmek, dikey motion |
| [09-pahali-dersler](skill/ajanla-video-kurgu/references/09-pahali-dersler.md) | Pahalıya patlayan beş ders ve arıza kataloğu |
| [10-baslangic-kiti](skill/ajanla-video-kurgu/references/10-baslangic-kiti.md) | Araçlar ve linkler |
| [templates/](skill/ajanla-video-kurgu/templates) | Marka dosyası, pano haritası, bölüm brief'i, teslim formu, prompt sözleşmesi, beğenmeme defteri |

### Notlar: `notlar/`

| Dosya | Ne |
|---|---|
| [bolumler.md](notlar/bolumler.md) | Videonun bölümleri, kısa notlar ve skill'deki karşılıkları |
| [transkript.md](notlar/transkript.md) | Tam transkript, zaman damgalı |

---

## Üç cümlede

1. Bizi hızlandıran şey ajanlar değil, etraflarına kurduğumuz düzen.
2. Aynı hatayı iki kez yapıyorsan onu nota değil koda yaz: kod geçmezse video çıkmaz.
3. Son söz sende: ne transkripte ne ajanın raporuna körü körüne güven.

---

## Kaynak ve not

- Pano haritası ve kapı fikri Sirio'nun açık kaynak kurgu sisteminden: https://github.com/sirioberati/YouTube-AI-Video-Editing-System
- Video Topview sponsorluğundaydı. Görsel ve video üretimi videoda Topview eklentisi üzerinden yapıldı; bu notlar herhangi bir üretim aracına bağlı değil.
- Araç ve model adları zamanla eskiyecek. Mantık kalacak.

Avenox: [YouTube](https://www.youtube.com/@avenoxai) · [X](https://x.com/Avenoxai) · [GitHub](https://github.com/avenoxai) · [avenox.lol](https://avenox.lol)
