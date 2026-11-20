# İzmir Asistanı

Hava durumuna bakan, ne giyeceğini söyleyen, şehirde ne olduğunu arayan ve seni tanıdıkça daha iyi cevap veren kişisel bir asistan. n8n **Agents** ile kuruyoruz, n8n'in kendi sohbet ekranında (**Test** modu) konuşuyoruz.

## Checkpoint'ler

| # | Ne yapıyorsun | Agents'ın hangi parçası | Kopyalanacak dosya | "Çalıştı" testi |
|---|---------------|-------------------------|---------------------|-----------------|
| 1 | Assistant'a tarif ederek agent'ı kurdur | Assistant · instructions · model | [1-instructions.md](1-instructions.md) | "Merhaba, ne yapabilirsin?" sorusuna cevap geliyor |
| 2 | Hava durumu aracı + web arama ekle | tools · web search | [2-hava-durumu-araci.md](2-hava-durumu-araci.md) | "Yarın Alsancak'ta ne giysem?" gerçek sıcaklıkla cevaplanıyor |
| 3 | "Sabah brifi" skill'i + hafıza | skills · memory | [3-skill-sabah-brifi.md](3-skill-sabah-brifi.md) | Yeni sohbette tercihini hatırlayıp brif formatında cevap veriyor |
| Bonus | Her sabah 08:00'de brif | triggers · schedule | [3-skill-sabah-brifi.md](3-skill-sabah-brifi.md#bonus-her-sabah-0800) | Hızlı bitirenler için |

Her checkpoint'te deneyeceğin sorular: [ornek-sorular.md](ornek-sorular.md)

## Agent sayfasında neler var?

| Alan | Ne işe yarar |
|------|--------------|
| **Instructions** | Agent'ın kim olduğu, nasıl konuşacağı, neyi yapıp neyi yapmayacağı |
| **Model** | Düşünen beyin. Trial'da hazır seçili gelir (GPT-5.6 Terra · Gateway credits), API key gerekmez |
| **Skills** | "Şu işi şöyle yap" diye paketlenmiş tarif. Gerektiğinde açılır |
| **Triggers** | Agent nerede ve ne zaman çalışır: **Add channel** (Telegram vb.) · **Add schedule** (belirli saatte kendi kendine) |
| **Capabilities** | Agent'ın dünyaya dokunduğu eller: **Add tool** (API çağrısı, tablo, mail) · **Add workflow** · **Add sub-agent** |
| **Web search** | Capabilities'in altında. Güncel bilgiyi internetten arar. **Varsayılanı Off** |
| **Memory** | **Session memory** hep açık (sohbet içinde hatırlar). **Cross-session memory** sohbetler arasında seni hatırlar, **varsayılanı kapalı** |
| **Build / Test** | Sohbet kutusunun altındaki düğme. **Build**: agent'ı tarif edip kurdurursun · **Test**: yayınlamadan önce agent'la konuşursun |

Agent sayfası iki parça: solda sohbet, sağda **Build · Knowledge · Sessions · Settings** sekmeleri. Bu workshop'ta her şey **Build** sekmesinde, yukarıdan aşağı: Model · Instructions · Skills · Triggers · Capabilities (Web search dahil) · Memory.
