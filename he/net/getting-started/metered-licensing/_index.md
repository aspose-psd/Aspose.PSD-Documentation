---
title: רישיון בהוגנה
type: מסמכים
weight: 80
url: /he/net/metered-licensing/
description: ספריית PSD של C# של Photoshop מאפשרת למפתחים להחיל מפתח מומדר שהוא מנגנון רישום חדש ויעשה שימוש לצד שיטת הרישום הקיימת.
---

{{% alert color="primary" %}} 

Aspose.PSD מאפשר למפתחים להחיל מפתח מומדר. זהו מנגנון רישום חדש. המנגנון ישמש לצד שיטת הרישום הקיימת. הלקוחות שרוצים לשלם בהתאם לשימוש בתכונות ה-API יכולים להשתמש ברישיון מומדר. לפרטים נוספים, ראה את [שאלות נפוצות על רישום מומדר](https://purchase.aspose.com/faqs/licensing/metered) סעיף.

{{% /alert %}} 
## **רישיון בהוגנה**
הנה השלבים הפשוטים לשימוש במחלקת Metered.

1. צור מופע של מחלקת Metered.
1. עבור פייתים ציבוריות ופרטיות לשיטת setMeteredKey.
1. בצע עיבוד (בצע משימה).
1. קרא לשיטה getConsumptionQuantity של מחלקת Metered.
1. זה יחזיר את כמות/כמות הבקשות ל-API שצרפת עד כה.

הנה קוד לדוגמה המדגים איך להגדיר פומבי ופרטי של מפתח מומדר.

{{< highlight java >}}

 // צור מופע של מחלקת PSD Metered

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// גש למאפיין setMeteredKey ועבור פייתי ציבורי ופרטי כפרמטרים

metered.SetMeteredKey("*****", "*****");



// קבל נתוני מומדר לפני שה-API מתקרא

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// הצג מידע

Console.WriteLine("כמות שצרפת לפני: " + amountbefore.ToString());

// קבל נתוני מומדר אחרי התקראות ל-API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// הצג מידע

Console.WriteLine("כמות שצרפת באחרי: " + amountafter.ToString());

{{< /highlight >}}
