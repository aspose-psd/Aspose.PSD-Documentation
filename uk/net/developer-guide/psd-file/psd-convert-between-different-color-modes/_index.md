---
title: Перетворення PSD між різними режимами кольорів
type: docs
weight: 50
url: /uk/net/psd-convert-between-different-color-modes/
---

Ви можете дізнатися про підтримувані режими кольорів у Aspose.PSD з цієї статті.

Наприклад, Aspose.PSD підтримує конвертацію від 8 до 16 біт на піксель і навпаки. Конвертацію ICC-профілю CMYK і інші конвертації з одного рівня розрядності в інший. Тут ви можете побачити приклади того, як конвертувати у відтінки сірого в файлі PSD.
## **Конвертувати з CMYK, RGB, у відтінки сірого в режим сірих відтінків**
Нижче поданий зразок коду демонструє, як зробити конвертацію з CMYK, RGB або відтінків сірого без використання Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **16-бітне зображення Photoshop у режим сірих 8 біт**
Але якщо вам потрібно конвертувати 16-бітне зображення Photoshop у режим сірих 8 біт, вам потрібно використовувати наступний фрагмент коду. 8 біт - це поширена розрядність в файлах PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **Конвертувати сірий в RGB**
Інший складний випадок - коли вам потрібно конвертувати зображення PSD у відтінках сірого до зображення RGB.

Сірий зображення мають лише один канал, але RGB зображення мають 3 канали: R - червоний, G - зелений, B - синій. Aspose.PSD може конвертувати сірий у RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
