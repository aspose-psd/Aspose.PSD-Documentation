---
title: Зміна зображень
type: docs
weight: 50
url: /uk/net/modifying-images/
---

## **Дітеринг для растрових зображень**
Дітеринг - це техніка створення ілюзії нових кольорів і відтінків шляхом зміни малюнка крапками, які насправді створюють зображення. Це найбільш поширений спосіб зменшення діапазону кольорів зображень до 256 (або менше) кольорів. Aspose.PSD надає підтримку дітерингу для класу [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), введенням методу Dither, який приймає два параметри. Перший - це тип DitheringMethod, який застосовується з двома можливими варіантами FloydSteinbergDithering та ThresholdDithering. Другим параметром для методу [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) є BitCount у форматі цілого числа. BitCount визначає розмір вибірки для результату дітерингу. Значення за замовчуванням - 1, що представляє чорний і білий, тоді як допустимі значення - 1, 4, 8, що генерують палітри з відповідно 2, 4 та 256 кольорами.

## **Налаштування яскравості, контрастності та гами**
Коригування кольорів у цифрових зображеннях - одна з основних функцій, яку надають більшість бібліотек обробки зображень. Коригування кольорів можна класифікувати наступним чином.

1. Яскравість відноситься до світлоти або темряви кольору. Збільшення яскравості зображення розгортає всі кольори, тоді як зменшення яскравості затемнює всі кольори.
1. Контраст відноситься до виділення об'єктів або деталей на зображенні. Збільшення контрастності зображення збільшує різницю між світлими і темними областями, так що світлі області стають світлішими, а темні області стають темнішими. Зменшення контрастності зробить світліші та темніші області приблизно однаковими, але загальне зображення стане більш однорідним.
1. Гамма оптимізує контраст та яскравість коротанини, що освітлює об'єкт на зображенні із непрямим освітленням.
### **Налаштування яскравості**
API Aspose.PSD для .NET надає метод [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) для класу [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), який можна використовувати для коригування яскравості зображення, передаючи ціле значення як параметр. Найвище значення параметра позначає яскравіше зображення. Ось початкове зображення та результативне зображення для порівняння.

## **Налаштування контрастності**
Метод [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast), реалізований класом [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), може використовуватися для налаштування контрастності зображення, передаючи значення float як параметр.

Найвище значення параметра позначає вищу контрастність у даному зображенні. Ось початкове зображення та результативне зображення для порівняння.

## **Налаштування гами**
Метод [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma), реалізований класом [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), має дві версії. Одне з перевантажень приймає одне значення float та виконує корекцію гами для коефіцієнтів червоного, синього та зеленого каналів. Тоді як інше перевантаження приймає три значення float, які представляють кожен коефіцієнт кольору окремо. Наведений нижче приклад коду демонструє, як коригувати гамму на зображенні.

## **Розмите зображення**
У цій статті показано використання Aspose.PSD для .NET для створення ефекту розмиття на зображенні. API Aspose.PSD надає ефективні та прості використанні методи для досягнення цієї мети. Aspose.PSD для .NET використовує клас [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions), щоб створити ефект розмиття на льоту. Клас [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) потребує значень радіусу та сигми для створення ефекту розмиття на зображенні. Кроки для виконання зміни розміру настільки прості:

1. Завантажте зображення за допомогою фабричного методу Load, що експонується класом Image.
1. Перетворіть зображення у [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Створіть екземпляр класу [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) з конструктором за замовчуванням або вкажіть значення радіусу та сигми у конструкторі.
1. Викличте метод [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter, вказавши прямокутник як межі зображення та екземпляр класу [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Збережіть результати.

Наведений нижче приклад коду демонструє, як створити ефект розмиття на зображенні.

## **Перевірка прозорості зображення**
У цій статті показано використання Aspose.PSD для .NET для перевірки прозорості зображення. Кроки для перевірки прозорості зображення настільки прості:

1. Завантажте зображення за допомогою методу фабрики [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2), що надається класом [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Перевірте непрозорість зображення, якщо непрозорість дорівнює нулю, зображення є прозорим.

Наведений нижче приклад коду демонструє, як перевірити, чи є зображення прозорим чи ні.

## **Реалізуйте стиснення втрат GIF**
Використовуючи Aspose.PSD для .NET, розробники можуть встановити різницю пікселів. Стиснення у форматі GIF базується на "словнику" рядків пікселів, які бачать. Звичайний кодер шукає у словнику найдовший рядок пікселів, які точно відповідають пікселям на зображенні. Поточний кодер вибирає найдовший рядок пікселів, який є "достатньо схожим" на пікселі на зображенні. Нижче наведено код демонстрації вказаної функціональності.

## **Реалізуйте бікубічне переформатування**
Переформатування означає зміну піксельних розмірів зображення. При зменшенні зразка ви видаляєте пікселі та, отже, видаляєте інформацію та деталі з вашого зображення. При збільшенні зразка ви додаєте пікселі. Photoshop додає ці пікселі за допомогою інтерполяції. Ця стаття демонструє, як ви можете виконати бікубічне переформатування за допомогою Aspose.PSD для .NET.

Нижче наведено код демонстрації вказаної функціональності.

## **Налаштування шару коригування кольору**
У цій статті показано використання Aspose.PSD для .NET для виконання **налаштування колірного балансу шару коригування** на зображенні. Шар коригування кольору балансу надає можливість вносити зміни до кольорів своїх зображень. Він представляє три кольорових канали та супутні кольори, і ви можете налаштувати баланс цих пар для зміни вигляду фотографії.

Нижче наведено код демонстрації вказаної функціональності.

## **Шар коригування інверсії**
У цій статті показано, як ви можете виконати **шар коригування інверсії** за допомогою Aspose.PSD для .NET. Шар коригування - це особливий вид шару, що використовується головним чином для корекції кольору. Замість власного вмісту вони налаштовують інформацію на рівнях, які перебувають під ними. Шар коригування інвертує кольори зображення, створюючи негативний ефект фотографії.

Нижче наведено код демонстрації вказаної функціональності.
