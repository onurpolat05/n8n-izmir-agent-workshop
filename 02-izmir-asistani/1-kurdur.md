# Checkpoint 1 · Agent'ı kurdur

Agent'ı elle kurmuyoruz: n8n'in **Assistant**'ına ne istediğimizi anlatıyoruz, o kuruyor.

## Yapıştır

Sol menüden **Assistant**'ı aç ve şu mesajın tamamını yapıştır:

```
"İzmir Şehir Asistanı" adında yeni bir agent oluştur. Türkçe, kısa ve
samimi konuşsun. Araçlardan gelen veriyi uydurmasın, bulamazsa söylesin.

Ona şu 4 HTTP Request aracını ekle (hepsi GET, API key gerekmez):

1. hava: İzmir için 3 günlük hava tahmini.
https://api.open-meteo.com/v1/forecast?latitude=38.437&longitude=27.143&daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,wind_speed_10m_max&timezone=Europe%2FIstanbul&forecast_days=3

2. hava_kalitesi: İzmir'de şu anki PM10, PM2.5 ve Avrupa hava kalitesi indeksi.
https://air-quality-api.open-meteo.com/v1/air-quality?latitude=38.437&longitude=27.143&current=pm10,pm2_5,european_aqi&timezone=Europe%2FIstanbul

3. deniz: Çeşme açıklarında dalga yüksekliği ve deniz suyu sıcaklığı.
https://marine-api.open-meteo.com/v1/marine?latitude=38.33&longitude=26.30&current=wave_height,sea_surface_temperature&timezone=Europe%2FIstanbul

4. nobetci_eczane: İzmir'deki bugünkü nöbetçi eczanelerin listesi (Bolge alanı semt adıdır).
https://openapi.izmir.bel.tr/api/ibb/nobetcieczaneler

Ayrıca web search'ü aç.
```

Assistant yarım dakika kadar düşünür, sonra agent'ı açar: sağda **İzmir Şehir Asistanı** sayfasını görürsün.

## Kontrol

Sağdaki **Build** sekmesinde şunları gör:

| Alan | Ne görmelisin |
|------|---------------|
| Model | Bir model seçili (ör. Claude Sonnet 5 · Gateway credits). API key gerekmez |
| Instructions | Assistant'ın senin için yazdığı talimat |
| Capabilities → Tools | **4 HTTP Request** |
| Web search | Açık |

## Test

Sağ üstteki **Test agent**'a tıkla ve yaz: **"Merhaba, ne yapabilirsin?"**

✅ Kendini İzmir Şehir Asistanı olarak tanıtıp hava, hava kalitesi, deniz ve eczane konusunda yardım edebileceğini söylüyorsa checkpoint 1 tamam.

## Takıldıysan

- Assistant agent'ı kurmadıysa mesajı bir kez daha gönder. Ya da **Overview → Build an agent** ile boş bir agent aç ve araçları [araclar.md](araclar.md)'deki tablodan elle ekle.
- Model alanı boşsa açılır menüden herhangi bir **Gateway credits** modelini seç.
