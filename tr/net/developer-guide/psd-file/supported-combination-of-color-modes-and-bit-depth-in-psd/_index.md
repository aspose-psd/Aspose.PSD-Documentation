---
title: PSD'de Renk Modları ve Bit Derinliği Desteklenen Kombinasyonu
type: docs
weight: 80
url: /tr/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Açıklama**
Aspose.PSD, Adobe Photoshop PSD dosyalarındaki herhangi bir Renk Modu ve Bit Derinliği kombinasyonunu açmayı destekler. Bu tür dosyaları açabilir ve dosyanın içeriğini değiştirmek için Düşük-Seviye API'sini kullanabilirsiniz. Ancak bazı daha az popüler kombinasyonlar özel sorunlar oluşturabilir, bunların bazıları Renk Modları Sınırlamaları ile ilgilidir.
## **PSD'de Renk Modları Ve Bit Derinliği Kombinasyonunun Desteklediği Dışa Aktarma Kombinasyonu Salt Okunur Modda**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Çoklu Kanal|Duoton|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Derinlik 1|Evet[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Derinlik 8|-|Evet|Evet|Evet|Evet|Hayır Q3-Q4|Hayır Q3-Q4|Evet[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Derinlik 16|-|Evet|-|Evet|Evet|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Hayır (Q3-Q4)|
|Derinlik 32|-|Evet*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Evet*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Bazı durumlarda küçük sorunlar
## **PSD'de Renk Modları Ve Bit Derinliği Kombinasyonunun Desteklediği Dışa Aktarma Kombinasyonu Düzenlenebilir Modda**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Çoklu Kanal|Duoton|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Derinlik 1|Evet|-|-|-|-|-|-|-|
|Derinlik 8|-|Evet|Hayır|Evet|Evet|Hayır Q3-Q4|Hayır Q3-Q4|Evet*|
|Derinlik 16|-|Evet|-|Evet|Evet*|-|-|Hayır (Q3-Q4)|
|Derinlik 32|-|Hayır (Q3-Q4)|-|Hayır (Q3-Q4)|-|-|-|-|
\* Bazı durumlarda küçük sorunlar

Belirli Bir Renk Modu / Bit Derinliği Kombinasyonunun desteğini ihtiyaç duyuyorsanız, [Aspose Forumları](https://forum.aspose.com/c/psd) üzerine gönderi yapabilirsiniz.
