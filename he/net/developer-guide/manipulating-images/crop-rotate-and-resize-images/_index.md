---
title: קיצוץ, הטיית, ושינוי גודל של תמונות
type: docs
weight: 40
url: /he/net/קיצוץ-הטיית-ושינוי-גודל-של-תמונות/
---

## **קיצוץ של תמונות**
קיצוץ התמונה מתייחס בדרך כלל להסרת החלקים החיצוניים של התמונה כדי לשפר את המסגון. הקיצוץ עשוי לשמש גם כדי לגזור חלק מהתמונה כדי להגביר את המוקד על אזור מסוים. ממשק ה-Aspose.PSD תומך בשתי גישות שונות לקיצוץ של תמונה: על ידי הזזות ומלבן.
### **קיצוץ על ידי הזזות**
מחלקת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) מספקת גרסה מעומצת של שיטת הקיצוץ שמקבלת 4 ערכים שלמים המציינים שמאל, ימין, עליון ותחתון. בהתבסס על ארבעת הערכים אלו, שיטת הקיצוץ מניעה את גבולות התמונה לקרב אל מרכז התמונה תוך ניתוש החלק החיצוני. קטע הקוד שלמטה מדגים איך לקצוץ תמונה על ידי הזזות.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **קיצוץ על ידי מלבן**
מחלקת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) מספקת גרסה נוספת של שיטת הקיצוץ שמקבלת מופע של מחלקת המלבן. ניתן לגזור חלק כלשהו של התמונה על ידי ספק את גבולות הרצויים לאובייקט המלבן. קטע הקוד שלמטה מדגים איך לקצוץ תמונה על ידי מלבן.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **להטות ולהיפוך תמונה**
‏Aspose.PSD עבור .NET היא ספרייה קלה לשימוש מכיוון שהיא מספקת שיטות פשוטות לביצוע פעולות מורכבות. לדוגמה, ‏Aspose.PSD עבור .NET סיפקה שיטת RotateFlip למחלקת הבסיס Image שלה אם יידרש לייצוב תמונה. ללא קשר לתבנית התמונה, הספרייה יכולה לבצע פעולת סיבוב ולהיפוך מסוים על התמונה.
### **לסובב תמונה**
שיטת Image.RotateFlip יכולה לשמש לסיבוב התמונה ב-90/180/270 מעלות ולהיפוך התמונה באופציה אופקית או אנכית. שיטת Image.RotateFlip מקבלת פרמטר של RotateFlipType שמציין את סוג הסיבוב וההיפוך שיש להחיל על התמונה. השלבים לביצוע סיבוב והיפוך הם פשוטים כפי שבמטה,

1. טען את התמונה באמצעות שיטת היצירה Load החשופה על ידי מחלקת Image.
1. קרא לשיטת Image.RotateFlip תוך ציון את RotateFlipType הנכון.
1. שמור את התוצאות.

קטע הקוד שלמטה מדגים איך לקבוע את מאפיין ה-RotateFlip של Image ואת תבניות ה-RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **לסובב תמונה בזווית ספציפית**
Aspose.PSD עבור .NET API מחשפת את שיטת מחלקת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate כדי לסייע למשתמשיה שרוצים לסובב תמונה בזווית ספציפית. להבדיל משיטת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, שיטת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate מקבלת שלושה פרמטרים:

1. זווית סיבוב: פרמטר מסוג float המציין את הזווית שבה תתבצע הסיבוב של התמונה. ערך חיובי מסובב את התמונה בכיוון השעון; ערך שלילי מבצע סיבוב נגד כיוון השעון.
1. לשנות ביחס: פרמטר מסוג בוליאני שמציין אם גודל התמונה צריך להשתנות לפי ההטלות של המלבן שסובב (נקודות הפינה). אם הוגדר כ-שקר, ממדי התמונה יישארו ללא שינוי ורק תכניות התמונה הפנימיים יסובבו.
1. צבע רקע: פרמטר מסוג Color מציין את הצבע שיש למלא ברקע של התמונה שסובבה.

קטע הקוד שלמטה מדגים את שימוש בשיטת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **שינוי גודל של תמונות**
מאמר זה מדגים את השימוש ב-Aspose.PSD עבור .NET לביצוע פעולת שינוי גודל על תמונה. ממשקי ה-API של Aspose.PSD חשפו שיטות יעילות וקלות לשימוש להשגת המטרה הזו. ‏Aspose.PSD עבור .NET חשפה את שיטת השינוי גודל של מחלקת התמונה שיכולה לשמש לשינוי גודל תמונות קיימות במהירות בזמן הרצה. ישנם שני מערכים נוספים של השיטה שיש להתאים לצרכי היישום.
### **שינוי גודל פשוט**
השלבים לביצוע שינוי גודל הם פשוטים כפי שבמטה:

1. טען את התמונה באמצעות שיטת היצירה Load החשופה על ידי מחלקת Image.
1. קרא לשיטת Image.Resize תוך ציון גובה ורוחב חדשים.
1. שמור את התוצאות.

קטע הקוד הבא מדגים איך לשנות את גודל התמונה.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **שינוי גודל עם הסט סוגי שינוי גודל**
ה-API של Aspose.PSD חשפה את Enumeration של ResizeType המשמש לצד Image.Resize לשם השגת תוצאות הרצויות. קטע הקוד הבא ממחיש את שימוש ב-Enumeration של ResizeType, בעוד פרטי איברי Enumeration זה ניתנים למציאה בתחתית דף זה.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



אם מתכוונים לקבל תוצאות איכותיות לאחר החידוש של הגודל אז מומלץ להשתמש תמיד ב-ResizeType.LanczosResample מאחר והוא יספק תוצאות באיכות גבוהה אך עשוי לפעול איטית יותר מ-ResizeType.NearestNeighbourResample. מצד שני, אלגוריתם ResizeType.NearestNeighbourResample משמש במיוחד להקטנה מהירה על חשבון איכות התמונה. שיטה זו יכולה להיות שימושית לייצוגי תמונה בזמן אמת או תהליכים דומים בהם נדרשת ביצועיות.
## **הקטנת תמונה בגודל פרופורציונלי**
ניתן להקטין תמונות על ידי מעבר ערכי גובה ורוחב חדשים כפרמטרים לשיטת Image.Resize , אך במקרה זה עליך לחשב את יחס התצוגה לבד. זה כי כאשר רוחב או גובה התמונה משתנים, התמונה מתאימה או מתמוססת על מנת למלא את הגודל החדש. אם השינויים ברוחב ובגובה של התמונה אינם יחסיים, זה עשוי להוביל לתוצאות מתוחות ומשופכות. מאמר זה מדגים את השימוש ב-Aspose.PSD עבור .NET API להקטנת תמונות על ידי העברת גובה או רוחב חדש, ובו זמן מאפשר ל-API לחשב באופן אוטומטי את הערך הפרופורציונלי השני.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Enumeration של ResizeType**
ResizeType קובע את סוג הקיט
