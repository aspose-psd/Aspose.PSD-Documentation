---
title: Python İle Sıfırdan PSD veya PSB Görüntü Oluşturma
weight: 100
type: docs
description: Python kullanarak Aspose.PSD'nin sıfırdan Psd Görüntü oluşturabileceğinin bir örneği
keywords: [psd oluştur, psb oluştur, yeni oluştur, katman oluştur, metin katmanı oluştur, psd api, python, kod örneği]
url: tr/python-net/create-psd-psb-images-from-scratch/
---

## **Genel Bakış**
Aspose.PSD kütüphanesini kullanarak Python ile sıfırdan bir PSD veya PSB dosyası oluşturmak için aşağıdaki adımları izleyebilirsiniz:

Gerekli modülleri ve sınıfları Aspose.PSD kütüphanesinden içe aktarın:
```python
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Çıkış dosya adını ve yolunu belirtin:

```python
outputFile = "CreateFileFromScratchExample.psd"
```

İstenen boyutlara sahip bir PSD görüntüsü oluşturun:

```python
with PsdImage(500, 500) as img:
```

Düzenli bir PSD katmanı ekleyin ve grafik API'sını kullanarak güncelleyin:

```python
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Metin katmanı oluşturun:
```python
textLayer = img.add_text_layer("Örnek Metin", Rectangle(200, 200, 100, 100))
```

Metin katmanına bir gölge efekti ekleyin:
```python
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

PSD dosyasını kaydedin:
```python
img.save(outputFile)
```

Bu kod, 500x500 piksel boyutlarında bir PSD görüntüsü oluşturur. Düzenli bir katman ekler ve bir kalem ve fırça kullanarak üzerinde bir elips çizer. Ardından "Örnek Metin" metinli bir metin katmanı ekler ve ona bir gölge efekti uygular. Son olarak, belirtilen çıkış dosya adıyla PSD dosyasını kaydeder.

Bu kodun çalışması için Python ortamınızda Aspose.PSD kütüphanesinin kurulu ve düzgün bir şekilde yapılandırılmış olması gerektiğini unutmayın. Kütüphaneyi nasıl kurup kullanılacağına dair daha fazla bilgi için resmi Aspose.PSD belgelerine başvurabilirsiniz.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
