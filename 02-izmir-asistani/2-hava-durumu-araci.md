# Checkpoint 2 · Hava durumu aracı + web arama

Agent'a iki "el" veriyoruz: gerçek hava tahmini ve güncel bilgi için internet araması.

## 2a · Hava durumu aracı (Open-Meteo, API key gerekmez)

Build sekmesinde **Capabilities → Add tool → HTTP Request** seç ve şunları doldur:

| Alan | Değer |
|------|-------|
| Tool adı | `hava_durumu` |
| Açıklama | aşağıdaki metin |
| Method | `GET` |
| URL | aşağıdaki URL |

**Açıklama** (agent bu metni okuyarak aracı ne zaman kullanacağına karar verir, bu yüzden önemli):

```
İzmir için önümüzdeki 3 günün hava tahminini getirir: en yüksek/en düşük
sıcaklık (°C), yağmur olasılığı (%), en yüksek rüzgâr (km/s).
Hava durumu ya da "ne giysem" sorulduğunda mutlaka bu aracı kullan.
```

**URL**, sabit İzmir merkez (en kolayı):

```
https://api.open-meteo.com/v1/forecast?latitude=38.437&longitude=27.143&daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,wind_speed_10m_max&timezone=Europe%2FIstanbul&forecast_days=3
```

### Semt bazlı sürüm (bitirenler için)

Koordinatları agent'ın kendisi doldursun. URL'yi şununla değiştir:

```
https://api.open-meteo.com/v1/forecast?latitude={{ $fromAI('enlem', 'Semtin enlemi', 'number') }}&longitude={{ $fromAI('boylam', 'Semtin boylamı', 'number') }}&daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,wind_speed_10m_max&timezone=Europe%2FIstanbul&forecast_days=3
```

Sonra Instructions'ın sonuna şu tabloyu ekle:

```
Semt koordinatları (enlem, boylam):
Alsancak 38.437, 27.143 · Bornova 38.462, 27.216 · Karşıyaka 38.455, 27.110
Buca 38.388, 27.175 · Urla 38.323, 26.765 · Çeşme 38.323, 26.303
Semt söylenmezse Alsancak'ı kullan.
```

<!-- [DOĞRULA 19 Kas] Agents node tool'unda $fromAI çalışıyor mu? Çalışmıyorsa semt sürümünü repodan kaldır. -->

## 2b · Web arama

Build sekmesinde, Capabilities'in en altındaki **Web search** varsayılan olarak **Off**. Açılır menüden aç. Etkinlik, ulaşım, nöbetçi eczane gibi güncel bilgileri buradan bulur.

<!-- [DOĞRULA 19 Kas] Trial'da web search modele bağlı (provider auto/native). Çalışmazsa bu adımı atla, checkpoint yalnız hava durumuyla tamamlanır. -->

## Test

**Test** modunda yeni bir sohbet aç:

- **"Yarın Alsancak'ta ne giysem?"** → Gerçek sıcaklık ve somut bir öneri gelmeli.
- **"Bu hafta sonu İzmir'de ne etkinlik var?"** → Kaynak adıyla birlikte cevap gelmeli.

✅ Execution / oturum detayında `hava_durumu` aracının çağrıldığını görüyorsan checkpoint 2 tamam.

Bak: Agent hangi aracı ne zaman kullanacağına **kendisi** karar verdi. W1'de bu kararı sen vermiştin.
