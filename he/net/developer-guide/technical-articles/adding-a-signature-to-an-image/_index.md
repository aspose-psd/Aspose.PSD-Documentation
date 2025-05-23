---
title: להוספת חתימה לתמונה
type: docs
weight: 70
url: /he/net/adding-a-signature-to-an-image/
---

## **הוספת חתימה**


להוספת חתימה לתמונה נדרשת לעיתים קרובות כדי לחתום על התמונות דיגיטלית וכדי למנוע זיוף. גם ניתן לחשוב על טיפול בתמונה כאילו היא מוצגת בגלריה. כל שהסיבה, ממשקי ה-Aspose.PSD מספקים את היכולת להוסיף חתימה לתמונה באמצעות מנגנון הפשוט ביותר כפי שמוסבר להלן. שימו לב, הדוגמה משתמשת ב-[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כיתה כדי לצייר תמונה נוספת עם חתימה על משטח התמונה המקורית. כדי להדגים את הפעולה, נטעין תמונת PSD מהדיסק ונצייר תמונה נוספת כחתימה על משטח התמונה המקורית באמצעות מתודת ה-DrawImage של המחלקה [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage). נשמור את התוצאה בתצורת PNG באמצעות מחלקת [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions). להלן דוגמת קוד שמדגימה איך להוסיף חתימה לתמונה. קטע הקוד לדוגמה הופרד לחלקים כדי להקל על ההבנה. בצעד אחר צעד, הדוגמה מראה איך:

- מאטעין את התמונות הראשית והמשנית (חתימה).
- יוצר ומאתחל אובייקט של Graphics.
- צייר תמונה באמצעות מתודת DrawImage של המחלקה Graphics.
- שומר את התוצאה בתצורת PNG.

### **דוגמאות לתוכניות**
#### **טעינת תמונות**
ראשית, צרו אינסטנסיה של מחלקת Image כדי לטעון את תמונות הדוגמה מהדיסק.
#### **יצירה ואתחול אובייקט גרפי**
לאחר טעינת התמונות, צור ואתחל אובייקט של מחלקת Graphics בעת השימוש באובייקט של התמונה הראשית.
#### **ציור תמונה משנית על התמונה הראשית**
לאחר טעינת התמונות, באמצעות מתודת הDrawImage של מחלקת Graphics, הוסף את התמונה המשנית על התמונה הראשית. ישנן מספר גרסאות של מתודת DrawImage שמקבלות אובייקט של התמונה כפרמטר ראשון כאשר כל הפרמטרים האחרים מתאימים למיקום שבו יש לצייר את התמונה. לצורך הדגמה, הקוד הבא משתמש בגרסת המוטעת של DrawImage שמקבלת אובייקט של Point כפרמטר שני ומנסה לצייר את החתימה בפינה הימנית למטה של התמונה הראשית.
#### **שמירת התמונה**
לבסוף, שמור את התמונה בחזרה לדיסק המקומי כקובץ PNG באמצעות מחלקת PngOptions.
#### **המקור המלא**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
