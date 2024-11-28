---
title: המרת מרחב צבע עבור JPEG דרך פרופילי ICC
type: docs
weight: 60
url: /he/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **ניהול צבע עבור פורמט JPEG**


מאמר זה מדבר על השימוש בפרופילי ICC על מנת לבצע את ניהול מרחב הצבעים בעת עיבוד פורמט JPEG בעזרת פעולות ה-Aspose.PSD API. מרחב הצבעים הפנימי של JPEG הוא YCbCr, אך יש באפשרות [פורמט](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) זה גם לכלול מרחבי צבע כגון Grayscale, RGB, CMYK ו- YCCK לאחסון מטא-נתוני התמונה. פעולות ה-API של Aspose.PSD מתבצעות בעיקר במרחב RGB לכן על ה-API לבצע המרות מרחב צבע לכיוון שלא תאודו נכון את קבצי ה-JPEG. ההמרות מ-Grayscale ל-RGB ומ-YCbCr ל-RGB ניתן לעשות באמצעות המרות מתמטיות, אך מרחבי צבע כגון CMYK ו-YCCK לא ניתן להמיר בקלות למרחב RGB.

מתבצעת המרה ישירה מ-RGB ל-CMYK עבור תמונות JPEG שמשתמשות במרחב צבע CMYK. מצד שני, תמונות המשתמשות במרחב צבע YCCK דורשות המרה מ-RGB ל-CMYK ולאח''כ ל-YCCK, שכאשר ההמרה מ-CMYK ל-YCCK משתמשת בגרסת [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) שמופעלת על שלושת הערוצים הראשונים, משאירה את הערוץ האחרון ללא שינוי. בקצרה, על ה-API של Aspose.PSD לבצע המרה בין מרחבי צבע RGB ו-CMYK עבור שתי סוגי התמונות, והמרות [אלו מתבצעות באמצעות פרופילים ICC שהם בעצם טבלאות חיפוש המתארות את המאפיינים של צבע ועוזרות בהמרות הצבעים.


## **פרופילי ICC**
המנגנון להמרת ICC משתמש ב-"פרופילים" הממפים את מרחב הצבע המקורי למרחבי צבע תלת-מימדיים תלויי-תקן (CIELAB or CIEXYZ). Aspose.PSD יכולה להמיר נתונים למרחב צבע כפי שנדרש בעת שימוש בשני מרחבי צבע אלו עם פרופילים נוספים. לכן, להמרת ICC, המשתמש צריך לספק שני פרופילים - פרופיל RGB להגעה לתוך מרחב הצבע ה-СIE הפנימי ופרופיל CMYK להגעה לז'יגות צבע ה-CMYK. על מנת להשיג המרה מ-CMYK ל-RGB, על המשתמש להחליף פרופילים, הכולל; להשתמש בפרופיל CMYK כפרופיל מקור ובפרופיל RGB כפרופיל יעד. 
## **המרת צבע ל-JPEG דרך פרופילי ICC**
ה-API של Aspose.PSD מעלים את הפרטים, ומספק מנגנון קל לשימוש לציון פרופילי ICC באמצעות [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions) class. כמו כן, Aspose.PSD משתמשת בפרופילים המדגימים של SWOP, CMYK ו-SRGB המוטבעים בלב הקוד, לכן במקרי השימוש המקובלים ביותר, למשתמש אינו צריך לחפש לפרופילים ספציפיים. קיים חסרון בתיקונים אלו, כלומר; המרות מרחבי צבע אלו הן לא הפיכות מחדש כי אינם ניתנים לצפייה בצבע זהה לאחר המרה מ-RGB ל-CMYK ולאחר מכן מ-CMYK ל-RGB עקב מרחבי צבע לא מתאימים ופרופילי צבע שונים. קטע הקוד הבא מדגים את שימוש ה-API של Aspose.PSD ל-.NET לציון פרופילי צבע RGB ו-CMYK עבור תמונת YCCK JPEG. בדוגמה למטה פרופילי הצבע RGB ו-CMYK משתנים והתמונה נשמרת במרחב צבע YCCK. כדאי לשים לב כי פרופילי [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) ו-[CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) properties יעבדו לשינוי נתוני הפיקסלים למרחב הצבע YCCK. כל מרחבי הצבע האחרים אינם מביאים את פרופילי הצבע לעדכון הנתונים הצבעות.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


אם לא הוגדרו פרופילים, אז ה-API של Aspose.PSD ל-.NET ישתמש בפרופילים ברירת מחדל במקום. הדוגמה למטה משתמשת בתכונות פרופילים יעד שמשנות את מרחב הצבע היעד עבור רוב תמונות ה-JPEG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
