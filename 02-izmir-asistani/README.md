# İzmir Şehir Asistanı

Havaya, hava kalitesine, denize ve nöbetçi eczanelere bakan, şehirde ne olduğunu arayan ve seni tanıdıkça daha iyi cevap veren bir asistan. n8n **Agents** ile kuruyoruz ve n8n'in kendi test sohbetinde konuşuyoruz.

Komut ezberlemen gerekmiyor: tek bir soru soruyorsun, hangi kaynağa bakacağına agent karar veriyor.

## Checkpoint'ler

| # | Ne yapıyorsun | Agents'ın hangi parçası | Dosya | "Çalıştı" testi |
|---|---------------|-------------------------|-------|-----------------|
| 1 | Assistant'a tek mesajla agent'ı kurdur | Assistant · model · instructions · tools · web search | [1-kurdur.md](1-kurdur.md) | "Merhaba, ne yapabilirsin?" sorusuna cevap geliyor |
| 2 | Kurulanı oku, sonra dene | instructions · araç açıklaması · tool calls | [2-oku-dene.md](2-oku-dene.md) | "Kordon'da koşsam?" sorusunda iki araç birden çağrılıyor |
| 3 | "Sabah brifi" skill'i + hafıza | skills · cross-session memory | [3-skill-hafiza.md](3-skill-hafiza.md) | Yeni sohbette seni hatırlayıp brif formatında cevap veriyor |
| Bonus | Her sabah 08:00'de brif | triggers · schedule | [3-skill-hafiza.md](3-skill-hafiza.md#bonus-her-sabah-0800) | Hızlı bitirenler için |

Her checkpoint'te deneyeceğin sorular: [ornek-sorular.md](ornek-sorular.md) · Araçları elle eklemek için: [araclar.md](araclar.md)

## Agent sayfasında neler var?

Agent sayfasının sağında **Build · Knowledge · Sessions · Settings** sekmeleri var. Bu workshop'ta her şey **Build** sekmesinde, yukarıdan aşağı:

| Alan | Ne işe yarar |
|------|--------------|
| **Model** | Düşünen beyin. Trial'da hazır seçili gelir (**Gateway credits**), API key gerekmez |
| **Instructions** | Agent'ın kim olduğu, nasıl konuşacağı, neyi yapıp neyi yapmayacağı |
| **Skills** | "Şu işi şöyle yap" diye paketlenmiş tarif. Agent onu yalnız gerektiğinde açar |
| **Triggers** | Agent nerede ve ne zaman çalışır: **Add channel** (Telegram vb.) · **Add schedule** (belirli saatte kendi kendine) |
| **Capabilities** | Agent'ın dünyaya dokunduğu eller: **Tools** (API çağrısı, tablo, mail) · **Add workflow** · **Add sub-agent** |
| **Web search** | Capabilities'in altında. Güncel bilgiyi internetten arar. **Varsayılanı kapalı** |
| **Memory** | **Session memory** hep açık (aynı sohbetin içinde hatırlar). **Cross-session memory** sohbetler arasında seni hatırlar, **varsayılanı kapalı** |

Agent'la konuşmak için sağ üstteki **Test agent**'a tıkla. Yayınlamadan (Publish) önce her şeyi burada denersin.

## Kaynaklar

Hava, hava kalitesi ve deniz: [Open-Meteo](https://open-meteo.com) · Nöbetçi eczane: [İzmir Büyükşehir Belediyesi açık veri](https://acikveri.bizizmir.com). Hiçbiri API key istemez.
