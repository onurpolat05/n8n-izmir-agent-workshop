# Remix · Asistanı kendi işine uyarla

İskelet aynı kalıyor: **instructions + bir araç + bir skill + hafıza**. Değişen yalnızca ne iş yaptığı. Aşağıdakilerden birini seç ya da kendi fikrini dene.

## Çalışanlar için

### Müşteri ziyareti brifi
Toplantıdan önce firmayı araştırır ve tek sayfalık brif verir.

```
Instructions: Sen bir satış/iş geliştirme asistanısın. Bir firma adı
verildiğinde web aramasıyla firmayı araştır: ne yapıyor, büyüklüğü,
son haberleri, kimlerle çalışıyor. Bilgiyi kaynak adıyla ver, uydurma.
```
Skill: `ziyaret-brifi`, 5 satır: Firma ne yapıyor · Son 3 ayda ne oldu · Bizimle ilgisi · Sorulacak 2 soru · Dikkat.

### Sektör haber bülteni
Her sabah sektöründen 3 haber getirir ve "bu bizi neden ilgilendirir" diye yorumlar.

```
Instructions: Sen <sektör> sektöründe çalışan birinin haber asistanısın.
Web aramasıyla son 24 saatin en önemli 3 haberini bul, her biri için
tek satır özet + tek satır "bizi neden ilgilendirir" yaz.
```
Bonus: her sabah 08:00'de çalışan bir task.

### Toplantı hazırlık asistanı
Toplantının konusunu ve katılımcıları verirsin; gündem, sorulacak sorular ve olası itirazlar gelir.

## Öğrenciler için

### Staj başvurusu öncesi firma araştırması
```
Instructions: Sen bir kariyer asistanısın. Başvurulacak firmayı web
aramasıyla araştır, firmanın ne yaptığını ve son projelerini özetle,
mülakatta sorulabilecek 3 soruyu ve kullanıcının sorabileceği 2 soruyu öner.
```

### Ders çalışma koçu
Hafızasında hangi konuların zor geldiğini tutar ve her gün o konudan kısa bir soru sorar.

## Remix yaparken

1. **Önce instructions'ı değiştir:** agent kim, ne yapmaz?
2. **Araç gerekiyor mu?** Güncel bilgi için web search çoğu zaman yeterli.
3. **Tekrar eden çıktın varsa** (brif, özet, rapor) onu skill yap.
4. **Zorlayan bir soruyla test et:** bilmediğinde uyduruyor mu?

Bitirdiysen 60 saniyede salona göster.
