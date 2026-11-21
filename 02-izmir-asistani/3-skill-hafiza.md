# Checkpoint 3 · Skill + hafıza

**Instructions** agent'ın kim olduğunu anlatır. **Skill** ise belirli bir işi nasıl yapacağını anlatan paketlenmiş bir tariftir: agent onu yalnız gerektiğinde açar. Böylece talimat kısa kalır, iş tarifleri de tek tek geliştirilebilir.

## 3a · "Sabah brifi" skill'i

Build sekmesinde **Skills → Add skill** seç. Açılan pencerede en alttaki **Add manually** bağlantısına tıkla ve aşağıdaki üç alanı kopyala-yapıştır.

> Kısa yol: bu repodaki [`sabah-brifi/SKILL.md`](sabah-brifi/SKILL.md) dosyasını indirip pencerede **Upload SKILL.md** ile yükleyebilirsin. Üç alan dosyada hazır.

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
🌫️ Hava kalitesi: <Avrupa AQI değeri ve tek kelimelik yorum>
👕 Ne giy: <tek satır somut öneri>
🚲 Yol: <kullanıcının ulaşım tercihine göre tek satır not>
📍 Bugün İzmir'de: <web aramasından 1 etkinlik, kaynak adıyla>

Kurallar:
- Hava bilgisini hava aracından, hava kalitesini hava_kalitesi aracından al.
- Kullanıcının hatırladığın tercihlerini (ulaşım, semt, sevdiği şeyler) kullan.
- Etkinlik bulamazsan o satıra "bugün öne çıkan bir şey bulamadım" yaz,
  uydurma.
```

## 3b · Hafıza

Build sekmesinin en altında **Cross-session memory** düğmesini aç. Varsayılanı **kapalı**: kapalı kalırsa agent yeni sohbette seni unutur. (Session memory zaten hep açık, ama o yalnız aynı sohbetin içinde hatırlar.)

**Test agent**'ta kendini tanıt:

```
Bornova'da oturuyorum, işe bisikletle gidiyorum
ve kalabalıkları sevmem.
```

## Test

**Yeni bir sohbet** aç ve yaz: **"Sabah brifimi ver."**

✅ Brif yukarıdaki formatta geliyorsa, yol satırı bisiklete göre yazılmışsa ve etkinlik önerisi kalabalık değilse checkpoint 3 tamam.

Agent yeni sohbette seni hatırladıysa bu **hafızadır**. Formatı her seferinde tutturuyorsa bu da **skill**'dir.

## Bonus · Her sabah 08:00

Evde dene: Build sekmesinde **Triggers → Add schedule**. Zamanlanmış görevin çalışması için agent'ı yayınlaman (**Publish**) gerekebilir; salonda yayınlamıyoruz.

| Alan | Değer |
|------|-------|
| Zaman | Her gün 08:00 (Europe/Istanbul) |
| Görev | `Sabah brifimi hazırla.` |

Çıktısını **Sessions** sekmesinde görürsün. Eve dönünce Telegram'a bağlarsan ([04-bonus-telegram](../04-bonus-telegram/)) brif telefonuna gelir.

<!-- [DOĞRULA 20 Kas] Schedule'ın çalışması için agent'ın publish edilmesi gerekiyor mu? Gerekiyorsa bonusa "Publish et" adımı eklenmeli. -->
