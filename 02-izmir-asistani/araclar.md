# Araçları elle eklemek

Assistant araçları eklemediyse ya da bir aracı kendin eklemek istersen: Build sekmesinde **Capabilities → Tools → +** ile bir **HTTP Request** aracı aç, Method `GET` seç ve aşağıdaki üç alanı doldur. Hiçbiri API key istemez.

## hava

**Açıklama:** `İzmir için 3 günlük hava tahmini: en yüksek/en düşük sıcaklık (°C), yağmur olasılığı (%), en yüksek rüzgâr (km/s). Hava ya da "ne giysem" sorulduğunda kullan.`

```
https://api.open-meteo.com/v1/forecast?latitude=38.437&longitude=27.143&daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,wind_speed_10m_max&timezone=Europe%2FIstanbul&forecast_days=3
```

## hava_kalitesi

**Açıklama:** `İzmir'de şu anki PM10, PM2.5 ve Avrupa hava kalitesi indeksi (European AQI). Dışarıda spor, yürüyüş ya da hava kirliliği sorulduğunda kullan.`

```
https://air-quality-api.open-meteo.com/v1/air-quality?latitude=38.437&longitude=27.143&current=pm10,pm2_5,european_aqi&timezone=Europe%2FIstanbul
```

## deniz

**Açıklama:** `Çeşme açıklarında şu anki dalga yüksekliği (m) ve deniz suyu sıcaklığı (°C). Denize girmek, tekne ya da sahil sorulduğunda kullan.`

```
https://marine-api.open-meteo.com/v1/marine?latitude=38.33&longitude=26.30&current=wave_height,sea_surface_temperature&timezone=Europe%2FIstanbul
```

## nobetci_eczane

**Açıklama:** `İzmir'deki bugünkü nöbetçi eczanelerin listesi: ad, adres, telefon. Bolge alanı semt adıdır (ör. "BORNOVA 1"); kullanıcı bir semt sorarsa listeyi o semte göre filtrele.`

```
https://openapi.izmir.bel.tr/api/ibb/nobetcieczaneler
```

Kaynaklar: [Open-Meteo](https://open-meteo.com) (hava, hava kalitesi, deniz) · [İzmir Büyükşehir Belediyesi açık veri](https://acikveri.bizizmir.com) (nöbetçi eczane).
