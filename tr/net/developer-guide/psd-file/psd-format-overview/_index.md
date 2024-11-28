---
title: PSD Format belgesi
type: docs
weight: 60
url: /tr/net/psd-format-belgesi/
---

## **Tanım**
PSD, Photoshop Belgesi, grafik tasarım ve geliştirme için kullanılan Adobe Photoshop'un yerel dosya biçimini temsil eder.
## **Dosya Biçimi Özellikleri**
Bir PSD dosyasındaki veriler büyük-endian bayt sırasında saklanır. Bu, Windows platformunda okurken veya yazarken kısa ve uzun tamsayıların yerlerini değiştirmeyi ima eder. Photoshop dosya biçimi beş ana bölüme ayrılır. Bir bölümden diğerine geçmek için kullanılabilecek pek çok uzunluk belirleyici vardır. Uzunluk belirleyiciler genellikle en yakın 2 veya 4 baytlık aralığa yuvarlanmak üzere baytlarla dolgulanır. Beş ana bölüm şunlardır:

- Dosya Başlığı
- Renk Modu Verileri
- Görüntü Kaynakları
- Katman ve Maske Bilgisi
- Görüntü Verisi

Uyum için, verilerin bu bölümlerdeki tüm alanlara yazılması gerekmektedir, çünkü Photoshop tüm bölümü okumayı deneyebilir. Ayrıca, bir dosyaya yazılırken atlanan alanlara sıfırların yazılması gerektiğini ima eder. Uzunluk-sınırlı bölümlerdeki uzunluk alanı, okumayı ne zaman durduracağımıza karar vermek için kullanılmalıdır. Çoğu durumda, uzunluk alanı, takip eden bayt sayısını, kayıtları değil, gösterir. Bir dosya okunurken aşağıdaki noktalar hatırlanmalıdır.

- Tüm tablolardaki "Uzunluk" sütunundaki değerler bayt cinsindendir.
- Unicode dizesi olarak tanımlanan tüm değerler aşağıdakilerden oluşur:
- Dizenin karakter sayısını temsil eden 4 baytlık bir uzunluk alanı (bayt değil).
- Karakter başına iki bayt olan Unicode değerleri dizisi.
## **Biçim Özellikleri**
PSD dosyaları, resim katmanları, ayar katmanları, katman maskeleri, açıklamalar, dosya bilgileri, anahtar kelimeler ve diğer Photoshop-specifik öğeleri içerebilir. Photoshop dosyalarının varsayılan uzantısı.PSD'dir ve maksimum yükseklik ve genişliğe sahiptir 30.000 piksel ve iki gigabayt uzunluk sınırlaması
## **Nasıl Kullanılabilir**
1. PSD Dilimleme aracı olarak.
1. [PSD'yi](/psd/tr/net/psd-resmini-raster-biçime-dönüştürme/) HTML'ye dönüştürmek
1. E-posta için [PSD örneği](/psd/tr/net/psd-dosyalarını-otomasyon-iş-kartları-olarak-şablon-olarak-kullanma/)
1. PSD'yi belirli CMS HTML'ye dönüştürme
1. PSD Dosyasındaki Kimlik Çizimi (Polis Eskizi)
1. Şişeler, fincanlar, tişörtler vb. gibi ürünler için Akıllı Nesneler kullanarak yarı-3D önizleme resimleri oluşturma.
1. PSD'nin Hızlı düzenlemesi: Otomatik ton, Ön Ayarlar, Akıllı Nesne, Metin Katmanı Görüntü Kesimi

Ve çok daha fazlası. Aspose.PSD ile harika bir şey yaptıysanız, lütfen [Aspose Forumları](https://forum.aspose.com/) kullanarak vaka çalışmanızı bizimle paylaşın.


Ek örneklerden öğrenebileceğiniz diğer konular:

- [Vaka Çalışmaları](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Vitrinler](/psd/tr/net/showcases-html/)
