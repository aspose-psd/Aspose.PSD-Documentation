---
title: המרת PSD בין מצבי צבע שונים
type: docs
weight: 50
url: /he/net/psd-convert-between-different-color-modes/
---

ניתן ללמוד על מצבי הצבעים שנתמכים של Aspose.PSD מתוך מאמר זה.

Aspose.PSD, למשל, תומך בהמרה מ-8 ל-16 ביט לפיקסל ולהיפך. המרות פרופיל ICC של CMYK ושיחות אחרות מסוג אחד של עומק ביט לסוג אחר. כאן ניתן לראות דוגמאות לאיך להמיר לגרייסקייל בקובץ PSD.
## **להמיר מ-CMYK, RGB, גרייסקייל למצב צבע גרייסקייל**
קוד דוגמה המוצף להלן מדגים כיצד לבצע המרה מ-CMYK, RGB, וגרייסקייל בלעדי פוטושופ.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **תמונת פוטושופ 16 ביט למצב גרייסקייל 8 ביט**
אבל מה אם תרצה להמיר תמונת פוטושופ בגרייסקייל ב־16 ביט למצב גרייסקייל ב־8 ביט? עליך להשתמש בקטע הקוד הבא. 8 ביטים הם עומק ביט נפוץ בקבצי PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **להמיר גרייסקייל ל-RGB**
המקרה המורכב השני אם תרצה להמיר תמונת PSD בגרייסקייל לתמונת RGB.

התמונות בגרייסקייל מכילות רק ערוץ אחד, אך תמונות RGB מכילות 3 ערוצים: R - אדום, G - ירוק, B - כחול. Aspose.PSD יכולה להמיר גרייסקייל ל-RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
