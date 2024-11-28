---
title: עיבוד תמונות PNG
type: docs
weight: 40
url: /he/net/manipulating-png-images/
---

## **ציון שקיפות עבור תמונות PNG**
אחת היתרונות של שמירת תמונות בתבנית PNG היא שה־PNG יכולה לכלול רקע שקוף. Aspose.PSD for .NET מספקת את היכולת לציין שקיפות לתמונות ה־PNG ולתמונות רסטר בצורה שמוצגת בקטע הבא. ממשק ה־API של Aspose.PSD for .NET יכול לשמש להגדרת כל צבע כשקוף בעת יצירת תמונות PNG חדשות או המרת תמונות קיימות לתבנית PNG. לצורך כך, ממשק ה־API של Aspose.PSD for .NET חשף את המאפיין [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) ואת התבנית [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) שניתן להגדיר לצורך ציון כל צבע שישמש כשקוף בתמונת ה־PNG. קטע הקוד שמסופק מדגים כיצד להמיר תמונת PSD קיימת לתמונת PNG על ידי ציון הצבע הרצוי כשקוף.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **הגדרת רזולוציה לתמונות PNG**
Aspose.PSD for .NET מסופקת עם מחלקת ההגדרת רזולוציה שניתן להשתמש בה להגדרת הרזולוציה עבור כל פורמטי התמונה כולל PNG. מאמר זה מדגים את שימוש בממשק ה־API של Aspose.PSD for .NET להגדרת פרמטרי הרזולוציה האופקיים והאנכיים עבור פורמט התמונה PNG. קטע הקוד למטה טוען תמונת PSD קיימת וממיר אותה לתבנית PNG ובנוסף משנה את הרזולוציה.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **דחיסת קבצי PNG**
המבנה הגרפי הנייד (PNG) הוא פורמט דחיסה ללא אובדן להעברת דמי-נתונים מעל רשתות. כאשר אתה שומר תמונה כקובץ PNG בכל תוכנה, יתכן שיתבקש ממך לבחור רמת דחיסה בטווח של 0 עד רמה מקסימלית. הגדרת ערך זה בעצם מדחיסה את גודל הקובץ ולא מפחיתה את איכות התמונה. מאמר זה מתאר כיצד API של Aspose.PSD מאפשר לך לשלוט בגודל הקובץ של קבצי ה־PNG. API של Aspose.PSD ניתן לשימוש להגדרת רמות דחיסה עבור פורמט הקובץ PNG באמצעות מחלקת PngOptions שמכילה מאפיין int [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). המאפיין מקבל ערך בין 0 ל־9, כאשר 9 היא הדחיסה המרבית. קטע הקוד שמסופק למעלה מדגים כיצד להגדיר את רמות הדחיסה באמצעות API של Aspose.PSD for .NET.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **ציון עומק צבע עבור תמונות PNG**
עומק הביטים בהיסגרות הוא מספר הביטים שמשמשים לציוני צבע של פיקסל בתמונת Bitmap. כמו כל התבניות הביטמפ האחרות, עומק הצבע ב־PNG מיוצג גם הוא בביט, כמו 1־ביט (2 צבעים), 2־ביט (4 צבעים), 4־ביט (16 צבעים) ו־8־ביט (256 צבעים). API של Aspose.PSD for .NET ניתן לשימוש להגדרת עומק הביטים עבור תמונות PNG באמצעות מאפיין [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) שנחשף על ידי מחלקת PngOptions. כרגע, עומק הביטים יכול להיות מוגדר ב־1, 2, 4 או 8 ביטים עבור סוגי צבע אפורים ואינדקסיים. רק 8 ביטים נתמכים לסוגי צבע אחרים. קטע הקוד שמסופק מדגים כיצד להגדיר את עומק הביטים עבור תמונת PNG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **יישום שיטות סינון על תמונות PNG**
עומק הביטים בהיסגרת הוא מספר הביטים שמשמשים לציוני צבע של פיקסל בתמונת Bitmap. כמו כל התבניות הביטמפ האחרות, עומק הצבע ב־PNG מיוצג גם הוא בביט, כמו 1־ביט (2 צבעים), 2־ביט (4 צבעים), 4־ביט (16 צבעים) ו־8־ביט (256 צבעים). API של Aspose.PSD for .NET ניתן לשימוש להגדרת עומק הביטים עבור תמונות PNG באמצעות מאפיין בעל שם BitDepth שנחשף על ידי מחלקת PngOptions. כרגע, עומק הביטים יכול להיות מוגדר ב־1, 2, 4 או 8 ביטים עבור סוגי צבע אפורים ואינדקסיים. רק 8 ביטים נתמכים לסוגי צבע אחרים. קטע הקוד שמסופק מדגים כיצד להגדיר את עומק הביטים עבור תמונת PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **שינוי צבע רקע של תמונת PNG שקופה**
תמונות בתבנית PNG יכולות לכלול רקע שקוף. Aspose.PSD for .NET מספקת את היכולת לשנות את צבע הרקע של תמונת PNG שכוללת רקע שקוף. API של Aspose.PSD for .NET ניתן לשימוש להגדיר/לשנות צבע של תמונת PNG עם רקע שקוף. קטע הקוד שמסופק מדגים כיצד להגדיר/לשנות את צבע הרקע של תמונת PNG עם רקע שקוף.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
