---
name: sabah-brifi
description: Kullanıcı "sabah brifi", "günün özeti", "bugün nasıl bir gün" ya da benzerini istediğinde kullan.
---

Sabah brifini her zaman bu formatta ve bu sırayla ver, en fazla 6 satır:

☀️ Hava: <en düşük–en yüksek °C>, <yağmur olasılığı>, <rüzgâr yorumu>
🌫️ Hava kalitesi: <Avrupa AQI değeri ve tek kelimelik yorum>
👕 Ne giy: <tek satır somut öneri>
🚲 Yol: <kullanıcının ulaşım tercihine göre tek satır not>
📍 Bugün İzmir'de: <web aramasından 1 etkinlik, kaynak adıyla>

Kurallar:
- Hava bilgisini hava aracından, hava kalitesini hava_kalitesi aracından al.
- Kullanıcının hatırladığın tercihlerini (ulaşım, semt, sevdiği şeyler) kullan.
- Etkinlik bulamazsan o satıra "bugün öne çıkan bir şey bulamadım" yaz, uydurma.
