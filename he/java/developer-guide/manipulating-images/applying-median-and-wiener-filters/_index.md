---
title: החלת מסנן הממוצע ומסנן וינר
type: docs
weight: 10
url: /he/java/applying-median-and-wiener-filters/
---

## **החלת מסנן הממוצע ומסנן וינר**
המסנן הממוצע הוא טכניקת סינון דיגיטלית לא לינארית, המשמשת להסרת רעש. הפחתה זו של רעש היא שלב טיפול טיפולי טיפולי טיפולי שטרודה רגיל הפובי לשפר את תוצאות הטיפול המאוחר. מסנן וינר הוא המסנן הלינארי המיטבי ביותר לשגיאת MSE (שגיאה מרובעת בממוצע) תוצאתי עבור תמונות עם רעש תוספי ושחזור. באמצעות Aspose.PSD עבור מפתחי API ג'אווה ניתן להחיל מסנן ממוצע על תמונה כדי להוריד את הרעש ולהחיל מסנן וינר של גאוס על תמונות. מאמר זה מדגים כיצד ניתן להחיל את מסנן הממוצע ואת מסנן וינר גאוס על תמונות.

### **החלת מסנן הממוצע**
Aspose.PSD מספקת Class MedianFilterOptions להחלת מסנן על RasterImage. קטע הקוד שמוצג מטה מדגים איך להחיל מסנן ממוצע על תמונת רסטר.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **החלת מסנן וינר גאוס**
Aspose.PSD מספקת Class GaussWienerFilterOptions להחלת מסנן על RasterImage. קטע הקוד שמוצג מטה מדגים איך להחיל מסנן וינר גאוס על תמונת רסטר.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **החלת מסנן וינר גאוס לתמונה צבעונית**
Aspose.PSD מספקת Class GaussWienerFilterOptions גם לתמונות צבעוניות. קטע הקוד שמוצג מטה מדגים איך להחיל מסנן וינר גאוס על תמונה צבעונית.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **החלת מסנן וינר תנועה**
Aspose.PSD מספקת Class MotionWienerFilterOptions להחלת מסנן על RasterImage. קטע הקוד שמוצג מטה מדגים איך להחיל מסנן וינר תנועה על תמונת רסטר.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **החלת מסנן תיקון על תמונה**
מאמר זה מדגים את שימוש ה-Aspose.PSD עבור ג'אווה כדי לבצע מסנני תיקון על תמונות. ממשקי ה-API של Aspose.PSD חשפו דרכים יעילות ונוחות לשימוש כדי להשיג מטרה זו. Aspose.PSD עבור ג'אווה חשפה Class BilateralSmoothingFilterOptions ו- SharpenFilterOptions לפילטרציה. נדרש ל Class BilateralSmoothingFilterOptions מספר שלם כגודל. הצעדים לביצוע שינוי גודל הם פשוטים ככל המידת הבאה:


1. טען תמונה באמצעות השיטה המקיפה Load החשופה על ידי Image Class.
1. המר את התמונה ל-RasterImage.
1. צור מופעים של Class BilateralSmoothingFilterOptions ו- SharpenFilterOptions.
1. קרא לשיטת Filter של RasterImage בזמן שמציין מלבן כגבולות התמונה ומופע Class BilateralSmoothingFilterOptions.
1. קרא לשיטת Filter של RasterImage בזמן שמציין מלבן כגבולות התמונה ומופע Class SharpenFilterOptions.
1. התאם את הניגודות
1. הגדר בהירות
1. שמור את התוצאות.

קטע הקוד הבא מראה לך כיצד להחיל מסנן תיקון.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **שימוש באלגוריתם לחץ של בראדלי**
הערת הגעת תמונה משמשת ביישומים גרפיים. המטרה של הערת תמונה היא לסווג פיקסלים כ "כהה" או "אור". Aspose.PSD API מאפשר לך להשתמש בערת בראדלי בעת המרת תמונות. קטע הקוד הבא מראה לך כיצד להגדיר את ערך הסף ולהפעיל את אלגוריתם הערת בראדלי.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
