# Başlangıç kiti

Kurulumu ajana yaptır: "Whisper'ı indir, HyperFrames'i kur" demen yeter. Sonra görsel ve video için bir üretim eklentisi bağla.
Kendi ses kaydın yoksa bir seslendirme aracıyla (ör. ElevenLabs) ses koyabilirsin; ses verildiğinde ajan gerisini yapar.

| Araç | Ne işe yarar | Link |
|---|---|---|
| Claude Code | Ana ajan (tek şef) | https://github.com/anthropics/claude-code |
| Codex | İkinci kodlama ajanı | https://github.com/openai/codex |
| HyperFrames | HTML'den video: sahneler aslında web sayfası, kodla motion video bunun üstünde | https://github.com/heygen-com/hyperframes |
| Whisper | Açık kaynak transkript modeli | https://github.com/openai/whisper |
| mlx-whisper | Mac'te yerel, hızlı Whisper | https://github.com/ml-explore/mlx-examples/tree/main/whisper |
| FFmpeg | Kesim, birleştirme, ses ve video işleme | https://ffmpeg.org |
| auto-editor | Sessizlik kesimi | https://github.com/WyattBlue/auto-editor |
| Cap | Ekran kaydı | https://cap.so |
| video-use | Ham çekimi klasöre at, Claude kessin (benzer bir yaklaşım) | https://github.com/browser-use/video-use |
| avenoxbeyin | Açık kaynak ikinci beyin: kütüphane, notlar ve skill'ler sürekli orada çalışır | https://github.com/avenoxai/avenoxbeyin |

Görsel ve video modelleri (videodaki seçim, değişebilir): görselde GPT Image 2.5, videoda Seedance 2.5.
Videoda ikisi de Topview eklentisi üzerinden kullanıldı (video Topview sponsorluğundaydı).

## Notlar

- **Sürümleri sabitle.** HyperFrames gibi temel aracı belli bir sürümde tut, ara ara bilerek güncelle; çok değişmesini istemiyorsan kendiliğinden güncellenmesin.
- **Transkripti yerelde yap.** Ses dışarı çıkmaz, ek ücret ödemezsin.
- **Tek şef.** Bütün kurgu işinde tek bir ana ajanla konuş; diğerleri onun altında çalışsın.
- **Model seçimi.** Videodaki görüş: bu iş için Opus şart, GPT ve Gemini aynı kaliteyi vermiyor (18:48). Kendi denemenle doğrula. Ama bir videoda iki model birlikte de çalıştı (Opus yönetti, işin bir kısmını Codex tarafı aldı).
- **İkinci beyin.** Kütüphane, beğenmeme defteri ve skill'ler bir ikinci beyinde dursun; süreçler orada kendi kendine işler.
