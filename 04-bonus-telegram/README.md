# Bonus · Asistanı Telegram'a bağla (eve dönünce)

Salonda bunu yapmıyoruz: bot kurulumu zaman alıyor ve agent'ın yayınlanmasını (publish) gerektiriyor. Evde yaklaşık 10 dakika sürer.

## 1 · Bot oluştur (Telegram)

1. Telegram'da **@BotFather**'ı aç (mavi tikli olanı).
2. `/newbot` yaz.
3. Bota bir ad ver, ör. `İzmir Asistanım`.
4. Bir kullanıcı adı ver; `bot` ile bitmeli, ör. `izmir_asistanim_bot`.
5. BotFather sana bir **token** verir (`123456789:AA...`). Bunu kimseyle paylaşma; bu token'ı bilen herkes botunu kullanabilir.

## 2 · Agent'a bağla (n8n)

1. Build sekmesinde **Triggers → Add channel → Telegram** seç.
2. **Create new credential** ile Telegram credential'ı aç ve token'ı yapıştır.
3. Kaydet.

## 3 · Yayınla

Kanal, agent **Publish** edilene kadar pasif kalır. Agent sayfasında **Publish**'e bas.

## 4 · Dene

Telegram'da botunu aç, `/start` yaz, sonra **"Sabah brifimi ver."**

Checkpoint 3'teki task (her sabah 08:00) açıksa brif artık her sabah telefonuna gelir.

## Güvenlik notu

Bot herkese açıktır: kullanıcı adını bilen herkes ona yazabilir ve senin model kredini harcar. Agent'a yalnız senin Telegram ID'ne cevap vermesini söyleyebilirsin. Ya da işin bitince agent'ı unpublish et.
