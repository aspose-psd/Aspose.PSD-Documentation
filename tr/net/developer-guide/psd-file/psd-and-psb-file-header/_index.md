---
title: PSD ve PSB Dosya Başlığı
type: docs
weight: 40
url: /tr/net/psd-ve-psb-dosya-basligi/
---

## **Açıklama**
Adobe Photoshop dosya başlığı, Dosya Versiyonu (PSD için 1 ve PSB için 2), Kanal Sayısı, Renk Modu ve Bit Derinliği hakkında bilgiler içerir.

Aspose.PSD tarafından desteklenen Renk Modu ve Bit Derinliği Kombinasyonlarını ilgili makaleden öğrenebilirsiniz.


Dosya başlığı, görüntünün temel özelliklerini içerir.

|**Uzunluk**|**Açıklama**|
| :- | :- |
|4|İmza: Her zaman *"8BPS"* olarak eşittir|
|2|[PSD Versiyonu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): Her zaman PSD Dosyaları için 1 ve PSB Dosyaları için 2'ye eşittir. Aspose.PSD, Dosya Formatının sürümünü algılayabilir ve doğru şekilde okuyabilir|
|6|Ayrılmış: Sıfır olmalıdır|
|2|Görüntüdeki kanal sayısı, içindeki herhangi bir alfa kanalını da içerir. Desteklenen aralık 1 ile 56 arasındadır|
|4|Görüntünün yüksekliği piksel cinsinden. Desteklenen aralık 1 ile 30.000 arasındadır. PSB Dosyası, yüksekliği 300.000 piksele kadar destekler. PSB Dosyaları aynı zamanda Aspose.PSD tarafından da desteklenir|
|4|Görüntünün genişliği piksel cinsinden. Desteklenen aralık 1 ile 30.000 arasındadır. PSB Dosyası, genişliği 300.000 piksele kadar destekler. Büyük PSD/PSB dosyalarının toplu işlenmesi de Aspose.PSD tarafından desteklenir|
|2|Derinlik: Kanal başına bit sayısı. Desteklenen değerler 1, 8, 16 ve 32'dir. Ancak her Renk Modu her derinlikle çalışmaz|
|2|Dosyanın [PSD renk modu](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes). Desteklenen değerler: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.|
Bunu kontrol etmek için [PSD API Referansımıza](https://reference.aspose.com/psd) göz atabilirsiniz.
