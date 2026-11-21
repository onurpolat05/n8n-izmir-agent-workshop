# Checkpoint 2 · Oku ve dene

Agent bir dakikada kuruldu. Şimdi ne kurulduğuna bakıyoruz, çünkü bir agent'ı **okuyamıyorsan** ona güvenemezsin.

## 2a · Talimatı oku

Build sekmesinde **Instructions**'ı aç. Assistant senin tek paragraflık isteğini nasıl bir talimata çevirdi? Şunlara bak:

- Her araç için "ne zaman kullan" cümlesi var mı?
- "Uydurma" kuralı nasıl yazılmış?
- Eczane için "semte göre filtrele" diye bir not var mı?

## 2b · Bir aracın içine bak

**Capabilities → Tools → 4 HTTP Request**'e tıkla ve `hava_kalitesi`'ni aç. İki şey göreceksin:

| Alan | Ne işe yarıyor |
|------|----------------|
| **Açıklama** | Agent aracı **bu cümleyi okuyarak** seçiyor. URL'ye bakmıyor |
| **URL** | Aracın gerçekte çağırdığı adres |

## 2c · Dene

**Test agent**'ta yeni bir sohbet aç ve sırayla sor:

| Soru | Ne olmalı |
|------|-----------|
| Yarın akşam Kordon'da koşacağım, uygun mu? | **İki araç birden:** hava + hava kalitesi, sonra tek bir öneri |
| Bu gece Bornova'da açık eczane var mı? | `nobetci_eczane` çağrılır, yalnız Bornova'dakiler gelir |
| Hafta sonu Çeşme'de denize girilir mi? | Hava + deniz |
| Bu hafta sonu İzmir'de ne var? | Web search, kaynak adlarıyla |

Cevabın üstündeki **"tool calls"** satırına tıkla: agent hangi aracı, hangi sırayla çağırdı?

✅ Kordon sorusunda iki aracın çağrıldığını görüyorsan checkpoint 2 tamam.

Bak: Hangi aracın çağrılacağını sen söylemedin. Agent soruyu okudu ve **kendisi karar verdi**. Bir workflow'da bu kararı kuran kişi verir, her adımı o dizer.

## Deney (vaktin varsa)

`deniz` aracının açıklamasını şununla değiştir: `Döviz kurlarını getirir.` Sonra yeni bir sohbette "Çeşme'de deniz nasıl?" diye sor. Agent ne yapıyor? Açıklamayı geri almayı unutma.

<!-- [DOĞRULA 20 Kas] Deney: açıklama bozulunca agent gerçekten şaşırıyor mu, yoksa Instructions'taki araç listesine bakıp yine doğru aracı mı seçiyor? Sonuca göre deneyin metni ve beklenen sonuç yazılacak. -->
