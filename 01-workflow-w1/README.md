# W1 · Form'dan takip sistemine

Biri formu doldurur → bilgileri Google Sheets'e yazılır → kişiye özel teşekkür maili gider → başvuru kurumsalsa ekibe ayrıca bildirim düşer.

Salonda bunu kurmuyoruz; sahnede çalışan bir workflow'u birlikte inceliyoruz. Bu klasör **evde denemen için**: workflow'un nasıl düşündüğünü görmek istersen hazır dosyayı içeri alıp çalıştır.

## İçeri alma

1. n8n'de **Create workflow**'a tıkla.
2. JSON dosyasının içeriğini kopyala ve boş tuvale yapıştır (Ctrl/Cmd + V).
3. Sheets ve Gmail node'larında credential seç: **Sign in with Google**.
4. Sheets node'unda tabloyu seç. Yoksa önce Google Sheets'te boş bir tablo aç ve ilk satıra şu başlıkları yaz: `Ad Soyad · E-posta · Şirket / Okul · Başvuru Tipi · Mesaj · submittedAt`.

## Checkpoint'ler

| Dosya | Ne eklendi | "Çalıştı" testi |
|-------|-----------|-----------------|
| [cp1-form-sheets.json](cp1-form-sheets.json) | Form → Sheets | Formu doldur, tabloda yeni satırı gör |
| [cp2-tesekkur-maili.json](cp2-tesekkur-maili.json) | + Teşekkür maili | Kendi adresine adınla başlayan bir mail gelir |
| [cp3-kurumsal-bildirim.json](cp3-kurumsal-bildirim.json) | + IF: "Kurumsal" ise ekibe bildirim | "Kurumsal" seç, iki mail gelsin. "Bireysel" seç, tek mail gelsin |

CP3'te `Ekibe Bildirim` node'undaki `BURAYA-KENDI-MAILINI-YAZ@ornek.com` adresini kendi adresinle değiştir.

## Burada görülecek dört kavram

| Kavram | W1'de nerede |
|--------|--------------|
| **Trigger** | Başvuru Formu: workflow'u başlatan olay |
| **Node** | Her kutu tek bir iş yapar |
| **Credential** | Google'a bir kez izin verirsin, n8n saklar |
| **Expression** | `{{ $('Başvuru Formu').item.json['Ad Soyad'] }}`: bir önceki adımın verisini kullanmak |

Execution sekmesinden her adıma hangi verinin girdiğini ve hangisinin çıktığını gör. Workflow'un en güçlü yanı bu şeffaflık.

<!-- [DOĞRULA 19 Kas] Üç JSON'u temiz Cloud trial'a yapıştırıp test et: form alan adları ($json['Ad Soyad']) ve Sheets autoMap gerçek çıktıyla eşleşiyor mu. -->
