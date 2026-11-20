# Checkpoint 3 · Skill + hafıza

**Instructions** agent'ın kim olduğunu anlatır. **Skill** ise belirli bir işi nasıl yapacağını anlatan paketlenmiş bir tariftir; agent onu yalnız gerektiğinde açar. Böylece instructions kısa kalır ve iş tarifleri tek tek geliştirilebilir.

## 3a · "Sabah brifi" skill'i

Build sekmesinde **Skills → Add skill** seç.

**Adı:** `sabah-brifi`

**Ne zaman kullanılır** (açıklama):

```
Kullanıcı "sabah brifi", "günün özeti", "bugün nasıl bir gün" ya da
benzerini istediğinde kullan.
```

**Gövde:**

```
Sabah brifini her zaman bu formatta ve bu sırayla ver, en fazla 6 satır:

☀️ Hava: <en düşük–en yüksek °C>, <yağmur olasılığı>, <rüzgâr yorumu>
👕 Ne giy: <tek satır somut öneri>
🚲 Yol: <kullanıcının ulaşım tercihine göre tek satır not>
📍 Bugün İzmir'de: <web aramasından 1 etkinlik, kaynak adıyla>
💡 Öneri: <kullanıcının tercihlerine uyan tek bir küçük öneri>

Kurallar:
- Hava bilgisini mutlaka hava_durumu aracından al.
- Kullanıcının hatırladığın tercihlerini (ulaşım, beslenme, semt) kullan.
- Etkinlik bulamazsan o satırı "bugün öne çıkan bir şey bulamadım" diye yaz,
  uydurma.
```

## 3b · Hafıza

Build sekmesinin en altında **Cross-session memory** düğmesini aç. Varsayılanı kapalı; kapalı kalırsa agent yeni sohbette seni unutur. (Session memory zaten hep açık, o yalnız aynı sohbetin içinde hatırlar.)

**Test** modunda agent'a kendini tanıt:

```
Bornova'da oturuyorum, işe bisikletle gidiyorum, vejetaryenim
ve kalabalıkları sevmem.
```

## Test

**Yeni bir sohbet** aç (önceki sohbeti kapat) ve yaz: **"Sabah brifimi ver."**

✅ Brif yukarıdaki formatta geliyor, hava Bornova'ya göre, yol satırı bisiklete göre ve öneri vejetaryen ise checkpoint 3 tamam.

Agent yeni sohbette seni hatırladıysa bu hafızadır. Formatı her seferinde tutturuyorsa bu da skill'dir.

## Bonus · Her sabah 08:00

Hızlı bitirenler için: Build sekmesinde **Triggers → Add schedule**.

| Alan | Değer |
|------|-------|
| Zaman | Her gün 08:00 (Europe/Istanbul) |
| Görev | `Sabah brifimi hazırla.` |

Çıktısını **Sessions** sekmesinde görürsün. Eve dönünce Telegram'a bağlarsan ([04-bonus-telegram](../04-bonus-telegram/)) brif telefonuna gelir.

<!-- [DOĞRULA 20 Kas] Schedule'ın çalışması için agent'ın publish edilmesi gerekiyor mu? Gerekiyorsa bonusa "Publish et" adımı eklenmeli. -->
