---
title: שימוש בקבצי PSD כתבניות לאוטומציה - מקרה כרטיסי ביקור
type: docs
weight: 10
url: /he/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **סקירה**
מאמר זה מתאר מקרים נפוצים שבהם נדרש לעדכן שכבות מסוימות [בקובץ PSD](https://wiki.fileformat.com/image/psd/) באופן תכנותי, כאשר הקובץ PSD/PSB מכיל מבנה דומה לתבנית ידועה. זה ניתן לשימוש ליצירת מספר גדול של כרטיסי ביקור עבור אנשים שונים (מקרה כרטיסי ביקור). או שנדרש לבצע תרגום של קובץ ה-PSD לשפות שונות על ידי החלפת חומר גרפי מסוים בו.

לאחר קריאת המאמר זה תדעו איך ניתן לבצע את זה:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)

## **מקרה פשוט**
לדוגמה, יש לך תבנית PSD עם שמות קבצים ידועים. לכן, עליך לשנות, לעדכן או להחליף שכבת PSD דרך C#. לכך תצתרך לפתוח את קובץ התבנית באמצעות Aspose.PSD.

כיצד לפתוח קובץ PSD דרך C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)



לאחר מכן עלינו למצוא את השכבה שברצוננו להחליף על ידי שמה. הנה יישום פשוט לכך.

כיצד למצוא את השכבה בקובץ PSD על ידי שמה

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



כאשר השכבה נמצאת, נוכל לעדכנה בדרך רגילה, באמצעות [גרפיקה](https://reference.aspose.com/psd/net/aspose.psd/graphics):

כיצד לצייר על השכבה ב-PSD באמצעות גרפיקה

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

במקרה זה, אנו ציירים תמונת PNG חדשה [שנטענה](https://wiki.fileformat.com/image/png/) על השכבה הקיימת, כך שהנתונים הישנים יאבדו בקובץ החדש.

אבל מה אם נצטרך גם לעדכן טקסט? התהליך יהיה דומה. נמצא [שכבת טקסט](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) לפי שמה ונעדכן [באופן תכנותי את שכבת הטקסט בקובץ Photoshop](/psd/he/net/render-text-with-different-colors-in-text-layer/).

כיצד לעדכן שכבת טקסט בתוך Photoshop באמצעות C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



לסיום, עלינו לשמור את השינויים שלנו:

כיצד לשמור קובץ PSD ששונה באמצעות [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



התמונה המתקבלת:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **מקרה מורכב עם תכונות נוספות**
למעלה הצגנו את הדרך הפשוטה ביותר לשינוי תמונה בשכבה של קובץ PSD.

אך Aspose.PSD יכולה להציע תכונות נוספות מורכבות כגון הוספת שכבה חדשה, הסרת שכבות ישנות ועדכון של שכבת טקסט באמצעות סגנונות שונים בטקסט רב-שורות.

ניתן למצוא [שכבה](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) שברצוננו להחליף, למצוא את מיקומה ברשימת השכבות, להסיר אותה ולהוסיף שכבה חדשה לאחר יצירתה מ-[קובץ Jpeg](https://wiki.fileformat.com/image/jpeg/) באותו מקום.

יצירת שכבה חדשה מקובץ והכנסתה לתמונת PSD באמצעות [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



בסוף קטע הקוד של קובץ זה, אנו מתקנים את מיקומי השכבות ומצילים את מערך השכבות החדשים בתמונת Psd.

כיצד להעתיק מאפייני שכבת [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



ובסיום, עלינו לעדכן שכבות טקסט בתמונת PSD הקיימת על ידי C#. Aspose.PSD תומכת [בעדכון של שכבת טקסט באמצעות רכיבים](/psd/he/net/working-with-text-layers/). כל [רכיב טקסט](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) מכיל שילוב ייחודי של סגנון ותכונות פסקה.

כיצד להעתיק מאפייני שכבת [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



כתוצאה, שינינו את תבנית ה-PSD דרך הקוד עם שכבה חדשה מקובץ Jpeg, Png, J2k, Bmp, Gif או Tiff וטקסט [רב-שורות עם סגנונות שונים](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) בכל שורה.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
