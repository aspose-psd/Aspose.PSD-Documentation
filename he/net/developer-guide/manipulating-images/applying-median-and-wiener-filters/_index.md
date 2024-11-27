---
title: החלת מסנן הממוצע ומסנן וינר
type: docs
weight: 10
url: /he/net/applying-median-and-wiener-filters/
---

## **החלת מסנן הממוצע ומסנן וינר**
המסנן הממוצע הוא טכניקת סינון דיגיטלית לא לינארית, השימוש בה נפוץ להסרת רעש. הפחתת הרעש הזה היא שלב טיפול סטנדרטי לשפר את התוצאות של עיבודים מאוחרים. מסנן וינר הוא מסנן לינארי סטציונרי אופטימלי (בריבוע ממוצע בין השגיאות) לתמונות עם רעש תוספתי והמופויות בהם. באמצעות Aspose.PSD עבור מפתחי API של .NET ניתן להחיל מסנן ממוצע על התמונה ולהחיל מסנן רעש גאוס וינר על התמונות. מאמר זה מדגים כיצד ניתן להחיל את מסנן הממוצע ואת מסנן רעש גאוס וינר על תמונות.

### **החלת מסנן ממוצע**
Aspose.PSD מספקת מחלקת [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) כדי להחיל מסנן על [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). קטע הקוד שסופק למטה מדגים כיצד להחיל את מסנן הממוצע על תמונת ראסטר.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **החלת מסנן רעש גאוס וינר**
Aspose.PSD מספקת מחלקת [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) כדי להחיל מסנן על [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). קטע הקוד שסופק למטה מדגים כיצד להחיל את מסנן הרעש גאוס וינר על תמונת ראסטר.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **החלת מסנן רעש גאוס וינר לתמונה צבעונית**
Aspose.PSD מספקת מחלקת [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) גם לתמונות צבעוניות. קטע הקוד שסופק למטה מדגים כיצד להחיל את מסנן הרעש גאוס וינר על תמונה צבעונית.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **החלת מסנן רעש תנועה וינר**
Aspose.PSD מספקת מחלקת [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) כדי להחיל מסנן על [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). קטע הקוד שסופק למטה מדגים כיצד להחיל מסנן וינר תנועה על תמונת ראסטר.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **החלת מסנן תיקון על תמונה**
מאמר זה מדגים את השימוש ב-Aspose.PSD עבור .NET לביצוע מסנני תיקון על תמונה. APIs של Aspose.PSD חשפו שיטות יעילות וקלות לשימוש כדי להשיג מטרה זו. Aspose.PSD עבור .NET חשף את מחלקת [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) ואת מחלקת [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) לפילטרציה. מחלקת BilateralSmoothingFilterOptions דורשת מספר שלם כגודל. השלבים לביצוע כתה הם פשוטים כפי שמוצג להלן:

1. טען תמונה באמצעות שיטת היצירה Load שנחשפה על ידי מחלקת התמונה 
1. המר את התמונה ל-RasterImage
1. צור מופע של BilateralSmoothingFilterOptions ו- SharpenFilterOptions
1. קרא לשיטת [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) תוך ציון מלבן כגבולות תמונה ומופע מחלקת BilateralSmoothingFilterOptions
1. קרא לשיטת [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) תוך ציון מלבן כגבולות תמונה ומופע מחלקת SharpenFilterOptions
1. כוונן את הניגודות
1. הגדר בהירות
1. שמור את התוצאות.


## **שימוש באלגוריתם אחזור ברדלי**
אלגוריתם העיקול של התמונה משמש ביישומי גרפיקה. המטרה של העיקול של תמונה היא לסווג פיקסלים כ"כהים" או "בהירים". API של Aspose.PSD מאפשר לך להשתמש בעיקול הגרסה התחתונה בעת המרה של תמונות. קטע הקוד הבא מראה לך כיצד להגדיר את ערך העיקול ולהפעיל את אלגוריתם העיקול של ברדלי.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
