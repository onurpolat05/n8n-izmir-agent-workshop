# Örnek sorular

Her checkpoint'ten sonra bunları dene. Agent'ın cevabı kadar **nasıl** cevap verdiğine de bak: cevabın üstündeki "tool calls" satırına tıkla, hangi aracı çağırdı, hangisini çağırmadı?

## Checkpoint 1-2 sonrası

| Soru | Beklenen araç |
|------|---------------|
| Yarın akşam Kordon'da koşacağım, uygun mu? | hava + hava_kalitesi |
| Yarın Alsancak'ta ne giysem? | hava |
| Hafta sonu Çeşme'de denize girilir mi? | hava + deniz |
| Bu gece Bornova'da açık eczane var mı? | nobetci_eczane |
| Karşıyaka'da nöbetçi eczane hangisi, telefonu ne? | nobetci_eczane |
| Bu hafta sonu İzmir'de ne var? | web search |
| Konak'tan Karşıyaka'ya en hızlı nasıl giderim? | web search |

## Checkpoint 3 sonrası (skill + hafıza)

- Bornova'da oturuyorum, işe bisikletle gidiyorum ve kalabalıkları sevmem. *(bunu söyle, sonra yeni sohbet aç)*
- Sabah brifimi ver.
- Akşam dışarıda ne yapsam?

## Agent'ı zorlayan sorular (salonda birlikte)

- Yarın Mars'ta hava nasıl? *(aracı yanlış yere çağırıyor mu, sınırı biliyor mu?)*
- 15 gün sonra ne giyeyim? *(araç yalnız 3 günlük: uyduruyor mu, söylüyor mu?)*
- Antalya'da nöbetçi eczane hangisi? *(araç yalnız İzmir'i biliyor: ne diyor?)*
- Bana bir mail gönder. *(öyle bir aracı yok: ne diyor?)*

İyi bir agent "yapamam" demeyi bilir. Bu sorular onu test etmek için.
