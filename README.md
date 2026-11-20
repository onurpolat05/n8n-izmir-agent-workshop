# n8n İzmir Workshop: Uçtan Uca AI Agent

21 Kasım 2026 · FabrikaLab İzmir · n8n İzmir topluluğu

Bugün n8n'in **Agents** özelliğiyle kendine bir asistan kuruyorsun. Kod yazmıyorsun; takıldığın her yerde bu repodaki hazır metni kopyalayıp yapıştırarak devam edebilirsin.

## Akış

| Saat | Ne yapıyoruz |
|------|--------------|
| 13:00 | Kapı, check-in, ikram |
| 13:30 | Açılış |
| 13:40 | n8n nedir, workflow mantığı ([01-workflow-w1](01-workflow-w1/)) |
| 14:00 | Hesap kontrolü: herkes Agents sekmesinde mi? |
| 14:10 | Agents turu |
| 14:40 | Mola |
| 14:55 | Uygulama: İzmir asistanı ([02-izmir-asistani](02-izmir-asistani/)) |
| 15:45 | Remix: kendi işine uyarla ([03-remix](03-remix/)) |
| 16:10 | Kapanış |
| 16:20 | Network |

## Başlamadan önce

- **n8n Cloud deneme hesabı:** [n8n.io](https://n8n.io) üzerinden açılır. Daha önce deneme hesabı açtıysan yeni bir e-posta adresiyle aç.
- **Laptop ve şarj aleti**

## Workflow mu, agent mı?

> Adımlar belliyse **workflow**, karar gerekiyorsa **agent**. Gerçek sistemlerin çoğunda ikisi birlikte çalışır.

| | Workflow | Agent |
|---|----------|-------|
| Kim karar veriyor | Sen, kurarken | Model, çalışırken |
| Aynı girdi | Hep aynı sonuç | Benzer ama birebir aynı olmayan sonuç |
| İyi olduğu iş | Form → tablo → mail | "Yarın ne giysem?" gibi soru |
| Hata ayıklama | Kolay, her adım görünür | Daha zor, oturum kaydına bakılır |

## Klasörler

| Klasör | İçinde ne var |
|--------|---------------|
| [01-workflow-w1](01-workflow-w1/) | Form → Sheets → Gmail workflow'u, 3 checkpoint JSON'u |
| [02-izmir-asistani](02-izmir-asistani/) | Ana uygulama: instructions, hava durumu aracı, skill, örnek sorular |
| [03-remix](03-remix/) | Asistanı kendi işine uyarlama fikirleri |
| [04-bonus-telegram](04-bonus-telegram/) | Eve dönünce: asistanı Telegram'a bağla |

## Takıldım, ne yapayım?

1. Elini kaldır, masalardaki ekip yanına gelir.
2. İlgili checkpoint'in hazır metnini kopyala ve yapıştır.
3. Agent cevap vermiyorsa: sohbet kutusunun altında **Test** seçili mi bak, yeni bir sohbet aç, sonra sağ panelde Model alanının dolu olduğunu kontrol et.

## Etkinlikten sonra

- Geri bildirim formu: <!-- link -->
- n8n İzmir topluluğu: <!-- WA / LinkedIn linki -->
- Sonraki etkinlik: n8n Women+ İzmir, 12 Aralık
