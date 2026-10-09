# IZTECH RUN

İYTE kampüsünde geçen, Python temalı bir sonsuz koşu oyunu. Sınavları aş, quizlerin altından geç ve laptopundan `"damage"` göndererek bugları temizle. Yol boyunca kahve ve powerbank toplayarak koşuyu sürdür.

## Oynanış

Koşuya başlamadan önce karakterini seçebilirsin. İki karakterin de hızı ve yetenekleri aynı.

- **Can:** 3 canla başlarsın. Engellere veya buglara çarpmak bir can götürür; kahve bir can yeniler. En fazla 3 can taşıyabilirsin.
- **Batarya:** Laptopun 10 şarjla başlar. Her atış bir şarj harcar, powerbank iki şarj doldurur. Şarj 10'u geçmez.
- **Engeller:** Gündüz sınav kâğıtları ve havada beliren quizler, gece domuzlar ve sinekler çıkar. Yerdeki engellerden zıplayarak, quiz ve sineklerin altından çömelerek geçebilirsin.
- **Buglar:** Hem gündüz hem gece çıkar ve vurulabilirler. Diğer engeller mermileri durdurur ama hasar almaz. Çarpan kod yazısı harflere ayrılarak dağılır.
- **Tempo:** Oyun ilerledikçe hızlanır. Her 1.200 puanda gündüz ile gece arasında geçiş olur; her 2.400 puanlık tam döngüde hız biraz daha artar.

Koşu sonunda skorun ve kişisel rekorun gösterilir. Rekor tarayıcıda saklanır; başka cihazlara aktarılmaz ve tarayıcı verileri silinirse sıfırlanır.

## Kontroller

| Hareket | Tuş |
| --- | --- |
| Zıpla | Space / ↑ |
| Çömel | ↓ / S — basılı tut |
| Ateş et | F |
| Duraklat / devam et | Esc |

Telefonda ekrandaki Jump, Duck ve Fire düğmeleri kullanılır. Çömelme düğmesine basılı tutabilirsin. Duraklatma ekranından koşuyu yeniden başlatabilirsin.

## Kampüs

Bölüm binaları, kütüphane, yurtlar ve Teknopark, İYTE'den fotoğraflar temel alınarak piksel çizimlerle oluşturuldu. Mekânlar farklı sıralarla karşına çıkar; arka plandaki öğrenciler ve köpekler engel değildir.

Şenlik alanında gündüz stantlar ve sucuk sırası, gece konser vardır. Gün geçişleri kademelidir; şenlik alanı ekrandayken konser veya stant düzeni aniden değişmez. Gece lambalar yanar ve binaların bazı pencereleri aydınlanır.

Arayüz Türkçe ve İngilizce kullanılabilir. Koyu tema ile turuncu-beyaz açık tema arasında geçiş yapılabilir. Oyun sessizdir.

## Yerelde çalıştırma

Oyun HTML, CSS ve JavaScript ile yazıldı; çizimler Canvas 2D üzerinde oluşturulur. Paket kurulumu veya derleme gerekmez.

`dist/index.html` dosyasını tarayıcıda açabilirsin. Yerel sunucuyla çalıştırmak için, Python kuruluysa proje klasöründe:

```sh
python -m http.server 8000 --directory dist
```

Ardından [localhost:8000](http://localhost:8000) adresini aç.

## Dosyalar

| Dosya | İçerik |
| --- | --- |
| `dist/index.html` | Oyun ekranı, menüler ve rehber |
| `dist/style.css` | Temalar, arayüz ve mobil düzen |
| `dist/game.js` | Oyun döngüsü, kontroller, çarpışmalar ve skor |
| `dist/art.js` | Karakterler, nesneler ve sahne çizimleri |
| `dist/campus.js` | Kampüs binaları ve çevre detayları |
| `dist/festival.js` | Şenlik alanı, öğrenciler ve köpekler |
| `dist/i18n.js` | Türkçe ve İngilizce metinler |
| `tests/` | Oynanış ve çizim testleri |
| [COURSE_SOURCES.md](COURSE_SOURCES.md) | Oyundaki ders kodlarının kaynakları |

## Testler

Node.js kuruluysa proje klasöründe çalıştır:

```sh
node --test tests/*.test.cjs
```

Testler; can ve batarya kurallarını, çarpışmaları, mermi davranışını, gün döngüsünü, karakter pozlarını ve mekân sırasını kontrol eder.

---

Arda KARAHALİLOĞLU tarafından, İYTE Yazılım için geliştirildi.
