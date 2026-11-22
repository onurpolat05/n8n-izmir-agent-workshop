# n8n İzmir Workshop: Uçtan Uca AI Agent

21 Kasım 2026 · İzmir Büyükşehir Belediyesi İzLab Dijital Deneyim Merkezi · n8n İzmir topluluğu

Bugün n8n'in **Agents** özelliğiyle kendine bir İzmir şehir asistanı kuruyorsun: havaya, hava kalitesine, denize ve nöbetçi eczanelere bakıp tek soruna cevap veren bir agent. Kod yazmıyorsun; takıldığın her yerde bu repodaki hazır metni kopyalayıp yapıştırarak devam edebilirsin.

## Akış

| Saat | Ne yapıyoruz |
|------|--------------|
| 13:00 | Kapı, check-in, ikram |
| 13:30 | Açılış |
| 13:40 | Workflow mu, agent mı? Sahnede çalışan bir workflow |
| 14:00 | Hesap kontrolü: sol menüde Assistant'ı görüyor musun? |
| 14:10 | Agents turu |
| 14:40 | Mola |
| 14:55 | Uygulama: İzmir şehir asistanı ([02-izmir-asistani](02-izmir-asistani/)) |
| 15:45 | Remix: kendi işine uyarla ([03-remix](03-remix/)) |
| 16:10 | Kapanış |
| 16:20 | Network |

## Başlamadan önce

- **n8n Cloud deneme hesabı:** [n8n.io](https://n8n.io) üzerinden açılır. Daha önce deneme hesabı açtıysan yeni bir e-posta adresiyle aç.
- **Laptop ve şarj aleti**
- **WiFi:** `WizmirNET`. Şifre yok, ücretsiz kısa bir kayıtla bağlanılır.

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
| [01-workflow-w1](01-workflow-w1/) | Evde dene: Form → Sheets → Gmail workflow'u, 3 checkpoint JSON'u |
| [02-izmir-asistani](02-izmir-asistani/) | Ana uygulama: kurulum mesajı, 4 araç, skill, örnek sorular |
| [03-remix](03-remix/) | Asistanı kendi işine uyarlama fikirleri |
| [04-bonus-telegram](04-bonus-telegram/) | Eve dönünce: asistanı Telegram'a bağla |
| [sizden-gelenler](sizden-gelenler/) | Katılımcıların paylaştığı asistanlar ve remix'ler; senin PR'ını da bekliyor |

## Takıldım, ne yapayım?

1. Elini kaldır, masalardaki ekip yanına gelir.
2. İlgili checkpoint'in hazır metnini kopyala ve yapıştır.
3. Agent cevap vermiyorsa: sağ üstteki **Test agent** ile yeni bir sohbet aç, sonra Build sekmesinde Model alanının dolu olduğunu kontrol et.

## Etkinlikten sonra

- **Kurduğun asistanı paylaş:** [sizden-gelenler](sizden-gelenler/) klasörüne pull request aç. Git bilmesen de olur, nasıl yapılacağı klasörün içinde yazıyor.
- **Fotoğraflar:** [etkinlik albümü](https://drive.google.com/drive/folders/1wa__AUahMi9xtL5-mXGaVO7aU2w1T-eS). Senin çektiklerini de [Sizden Gelenler](https://drive.google.com/drive/folders/1FgobKYki5KV7LTy-6r-DLclmZa7JMXes) klasörüne bekliyoruz.
- Geri bildirim: [iki dakikalık form](https://docs.google.com/forms/d/e/1FAIpQLSfKn_iBt8m7M590Tcas1ryM2gccBqMTh605mBK0OnrxThqtMg/viewform). Bir sonraki etkinliğin konusunu buradan seçiyoruz.
- n8n Türkiye topluluğu: [LinkedIn grubu](https://www.linkedin.com/groups/39722002/). Sonraki etkinlikler burada duyuruluyor.
- Sonraki etkinlik: n8n Women+ İzmir, 12 Aralık
