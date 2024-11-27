---
title: קיטול, סיבוב ושינוי גודל של תמונות
type: docs
weight: 40
url: /he/java/crop-rotate-and-resize-images/
---

## **קיטול של תמונות**
קיטול של תמונה מתייחס בדרך כלל להסרת חלקי התמונה החיצוניים כדי לשפר את המיסגור. קיטול יכול לשמש גם לחיתוך חלק מהתמונה על מנת להעצים את המוקד על אזור מסוים. ממשק ה-Aspose.PSD תומך בשני גישות שונות לקיטול של תמונה: על ידי היסגרות וגם על ידי מלבן.
### **קיטול על ידי היסגרות**
מחלקת RasterImage מספקת גרסה נטענת של הפעולה Crop שמקבלת 4 ערכים שלמים המציינים שמאל, ימין, עליון ותחתון. בהתבסס על ארבעת הערכים הללו, פעולת ה- Crop מעבירה את גבולות התמונה לכיוון מרכז התמונה תוך התעלמות מהחלק החיצוני. קטע הקוד למטה מדגים איך לקטל תמונה על ידי היסגרות.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **קיטול על ידי מלבן**
מחלקת RasterImage מספקת גרסה נוספת של הפעולה Crop שמקבלת אינסטנס של מחלקת המלבן. ניתן לחתוך חלק מכל תמונה על ידי הגדרת הגבולות הרצויים לאובייקט המלבן. קטע הקוד למטה מדגים איך לקטל תמונה לפי מלבן.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **סיבוב והיפוך של תמונה**
Aspose.PSD עבור Java היא ספריה קלה לשימוש מאחר והיא מספקת שיטות פשוטות לביצוע פעולות מורכבות. למשל, Aspose.PSD עבור Java סיפקה את שיטת RotateFlip עבור מחלקת התמונה הבסיסית שלה אם היישום מחייב סיבוב של תמונה. בלתי תלוי בפורמט התמונה, הספריה יכולה לבצע סיבוב ו- Flip מסוים על התמונה.
### **סיבוב של תמונה**
שיטת Image.RotateFlip ניתן להשתמש בה כדי לסובב את התמונה ב-90/180/270 מעלות ולהיפך את התמונה אופקית או אנכית. Image.RotateFlip מקבלת פרמטר של RotateFlipType שמציין את סוג הסיבוב וההיפוך שיש להחיל על התמונה. השלבים לביצוע Rotate ו- Flip הם פשוטים כפי שמופיע למטה,

1. טען תמונה באמצעות שיטת היצרות Load המוצגת על ידי מחלקת Image.
1. הפעל את שיטת Image.RotateFlip תוך הגדרת סוג ה- RotateFlipType המתאים.
1. שמור את התוצאות.

דוגמה לקוד למטה מדגימה כיצד להגדיר את תכונת RotateFlip של תמונה ואת חברת RotateFlipType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **סיבוב של תמונה בזווית מסוימת**
ממשק ה-Aspose.PSD ל-Java מציע את שיטת הפעולה RasterImage.Rotate כדי לסייע למשתמשיה שרוצים לסובב תמונה בזווית מסוימת. לעומת שיטת RasterImage.RotateFlip, שיטת RasterImage.Rotate מקבלת שלושה פרמטרים:

1. זווית סיבוב: פרמטר מסוג float שמציין את הזווית שבה התמונה צריכה להיסובב. ערך חיובי מסובב את התמונה בכיוון השעון; ערך שלילי מבצע סיבוב נגד שעון.
1. הקטנת גודל באופן פרופורציונלי: פרמטר מסוג בוליאן שמציין האם גודל התמונה צריך להשתנות לפי ההשתקפויות של הנקודות הפינתיות של המלבן המסובב. אם הגדרתו כשקר יתנוון למידות התמונה ורק התוכן הפנימי של התמונה יסובב.
1. צבע רקע: פרמטר מסוג צבע שמציין את הצבע שיש למלא ברקע של התמונה הסובבת.

קטע הקוד למטה מדגים את השימוש בשיטת פעולה RasterImage.Rotate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **שינוי גודל של תמונות**
מאמר זה מדגים את שימוש ב-Aspose.PSD עבור Java לביצוע פעולת השינוי בגודל של תמונה. ממשקי ה-Aspose.PSD חשפו שיטות יעילות & קלות לשימוש להשגת מטרה זו. Aspose.PSD עבור Java חשפה את שיטת Resize למחלקת Image שניתן להשתמש בה לשינוי גודל של תמונות קיימות באופן דינמי. קיימות שתי גרסאות של שיטת Resize להתאמה לצרכי האפליקציה.
### **שינוי גודל פשוט**
השלבים לביצוע השינוי בגודל הם פשוטים כמו שמופיע למעלה:

1. טען תמונה באמצעות שיטת היצרות Load המוצגת על ידי מחלקת Image.
1. השתמש בשיטת Image.Resize תוך ציון גובה ורוחב חדשים.
1. שמור את התוצאות.

דוגמא לקוד מתחת מדגמת איך לשנות את גודל התמונה.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **שינוי גודל עם רשימת צורות שינוי גודל**
ממשק ה-Aspose.PSD חשף רשימת צורות של שינוי גודל שאפשר להשתמש בה עם Image.Resize כדי להשיג תוצאות הרצויות. קטע הקוד למטה מדגים את השימוש ברשימת צורות של שינוי הגודל, כאשר פרטי חברי רשימת הצורות של שינוי הגודל ניתן למצוא בתחתית עמוד זה.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



אם אתה מתכנן לקבל תוצאה באיכות לאחר החידוש, מומלץ להשתמש תמיד ב-ResizeType.LanczosResample מאחר שהוא יציב תוצאות איכותיות מאוד אף על פי שייעבוד לאט יותר מ-ResizeType.NearestNeighbourResample. בדיעבד, אלגוריתם ה-ResizeType.NearestNeighbourResample משמש במיוחד לכיווץ מהיר תוך פגיעה באיכות התמונה. שיטה זו עשויה להיות שימושית ליצירת תמונות ממוזערות בזמן אמת או תהליכים דומים בהם נדרשת ביצועיות.
## **שינוי גודל של תמונה בהתאמה פרופורציונלית**
באפשרותך לשנות את גודל התמונות על ידי העברת ערכי גובה ורוחב חדשים כפרמטרים לשיטת Image.Resize אך במקרה זה עליך לחשב את יחס הרוחב לגובה לבד. הדבר בגלל שכאשר הרוחב או הגובה של תמונה משתנים, התמונה מתאמצת או מתמחשטת כדי למלא את הגודל החדש. אם השינויים ברוחב ובגובה של תמונה אינם ממוספם זה עשוי להביא לתוצאה מתוחה ומשולשת. מאמר זה מדגים את השימוש ב-API של Aspose.PSD עבור Java לשינוי גודל של תמונות על ידי העברת לגובה או לרוחב בזמן שה-API מחשב עבורך את הערך הפרופורציונלי האחר. 



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **רשימת צורות שינוי הגודל**
ה-ResizeType קובע את סוג השהייה שיש לבצע על התמונה על פי המסנן הנבחר.

חברי רשימת
