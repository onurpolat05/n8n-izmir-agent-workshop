# Sizden gelenler

Workshop'ta kurduğun asistanı ya da evde uyarladığın bir remix'i burada paylaşırsan, bir sonraki etkinliğe gelen kişi boş sayfadan değil senin örneğinden başlar. Bitmiş olması gerekmiyor; yarım kalan bir deneme de, "şurada takıldım" notu da işe yarar.

## Ne gönderebilirsin

- Agent'ının **instructions** metni ve eklediğin **skill**
- Kullandığın araçların listesi (hangi API, hangi node)
- Agent'a sorduğun birkaç soru ve aldığın cevaplar (ekran görüntüsü de olur)
- Workflow kurduysan dışa aktarılmış **JSON** dosyası

## Klasör düzeni

Kendi adınla ya da GitHub kullanıcı adınla bir klasör aç, içine bir `README.md` koy:

```
sizden-gelenler/
└── kullanici-adin/
    ├── README.md          ← ne yaptın, neden, nasıl denenir
    ├── instructions.md    ← (varsa)
    ├── SKILL.md           ← (varsa)
    └── workflow.json      ← (varsa)
```

README'de üç şey yeterli: asistan ne iş yapıyor, hangi araçları kullanıyor, bir örnek soru ve cevabı.

## Nasıl gönderilir

**Git bilmiyorsan:** Bilgisayarında adını taşıyan bir klasör aç, dosyalarını içine koy. Bu klasördeyken (`sizden-gelenler/`) sağ üstteki **Add file → Upload files**'a tıkla, klasörü olduğu gibi sürükle bırak, en altta **Propose changes** de. GitHub senin adına bir kopya (fork) ve bir pull request açar; tek yapman gereken son ekranda **Create pull request**'e basmak.

**Git biliyorsan:** Repoyu fork'la, `sizden-gelenler/kullanici-adin/` klasörünü ekle, pull request aç.

Gelen PR'lara biz bakıp birleştiriyoruz.

## Göndermeden önce kontrol et

- **API anahtarı, şifre ya da token yok.** n8n'in dışa aktardığı JSON'da credential'ın kendisi değil, yalnız adı ve ID'si bulunur; ama bir node'un içine elle anahtar yazdıysan onu sil.
- **Kişisel veri yok.** Gerçek e-posta adresi, telefon numarası ya da müşteri bilgisi taşıyan ekran görüntüsünü bulanıklaştır.
- Fotoğraflar buraya değil, [Drive'daki Sizden Gelenler klasörüne](https://drive.google.com/drive/folders/1FgobKYki5KV7LTy-6r-DLclmZa7JMXes).
