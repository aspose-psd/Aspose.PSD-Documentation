---
title: PSD dosyalarındaki Katmanları Düzenlemek için Grafik API'sini Kullanma
weight: 100
type: docs
description: Aspose.PSD için Python'da Grafik API'sini kullanma örneği
keywords: [katmanı güncelle, daire çiz, elips çiz, dolgu daire çiz, grafik, psd api, python, kod örneği]
url: /tr/python-net/graphics-api/
---

## **Genel Bakış**
İlk olarak, PSD dosyasını Image.load() yöntemini kullanarak yüklemeniz veya sıfırdan bir Psd Image oluşturmanız gerekir. Örnekte, inputFile değişkeni PSD dosyanızın yolunu temsil eder ve loadOpt yüklemeyi seçeneklerini temsil eder (varsa).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Daha sonra, psdImage.layers[0] sözdizimini kullanarak PSD görüntüsünün ilk katmanına erişebilirsiniz. Bu size manipüle edebileceğiniz katman nesnesine bir referans sağlar.

```python 
layer = psdImage.layers[0]
```
Katmanı düzenlemek için, katmanı bir parametre olarak geçirerek bir Grafik nesnesi oluşturmanız gerekir. Bu nesne, şekiller çizmek ve fırçalar uygulamak için çeşitli yöntemler sağlar.

```python 
graphics = Graphics(layer)
```
Kod örneğinde, bir Pen nesnesi oluşturulurken, elips şeklinin kenarlık rengini ve kalınlığını tanımlar. Color.alice_blue sabiti rengi temsil eder ve ihtiyaca göre kalınlığı ayarlayabilirsiniz.

```python 
pen = Pen(Color.alice_blue)
```
Benzer şekilde, bir LinearGradientBrush nesnesi oluşturulurken, elips şeklinin doldurma rengini tanımlar. Rectangle(250, 250, 150, 100) elips şeklinin konumunu ve boyutunu temsil eder ve Color.red ve Color.aquamarine başlangıç ve bitiş renklerini temsil eder.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Elips şeklini katmana çizmek için graphics.draw_ellipse() yöntemini kullanabilirsiniz. Rectangle(100, 100, 200, 200) elips şeklinin konumunu ve boyutunu temsil eder.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Elips şeklini gradyan fırça ile doldurmak için graphics.fill_ellipse() yöntemini kullanabilirsiniz. Rectangle(250, 250, 150, 100) elips şeklinin konumunu ve boyutunu temsil eder.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Katmandaki istenilen değişiklikleri yaptıktan sonra, değiştirilmiş PSD görüntüsünü psdImage.save() yöntemini kullanarak kaydedebilirsiniz. Örnekte, psdName değişkeni değiştirilmiş PSD dosyasını kaydetmek için yolunuzu temsil eder.

```python 
psdImage.save(psdName)
```
Ayrıca, PngOptions sınıfını kullanarak PNG gibi diğer biçimlerde değiştirilmiş görüntüyü kaydedebilirsiniz. pngName değişkeni PNG dosyasını kaydetmek için yolu temsil eder.

```python 
psdImage.save(pngName, PngOptions())
```
Bu kadar! Aspose.PSD'nin Python için Grafik API'sini kullanarak PSD dosyalarındaki katmanları düzenli bir şekilde kullandınız. Resim düzenleme yeteneklerinizi artırmak için Aspose.PSD kütüphanesinin diğer özelliklerini ve işlevselliğini keşfetmekte özgürsünüz.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py" >}}
