---
title: Малювання зображень
type: docs
weight: 10
url: /uk/java/drawing-images/
---

## **Малювання ліній**
У цьому прикладі використовується клас Graphics для малювання форм ліній на поверхні зображення. Для демонстрації операції приклад створює нове зображення та малює лінії на поверхні зображення, використовуючи метод DrawLine, викладений класом Graphics. Спочатку ми створимо об'єкт PsdImage, вказавши його висоту та ширину.

Після створення зображення ми використовуємо метод Clear, викладений класом Graphics, щоб встановити його фоновий колір. Метод DrawLine класу Graphics використовується для малювання лінії на зображенні, що з'єднує дві структури точок. Цей метод має кілька варіантів перегрузки, які приймають екземпляр класу Pen та пари координат точок або структури Point/PointF як аргументи. Клас Pen визначає об'єкт, що використовується для малювання ліній, кривих та фігур. У класу Pen є кілька перегружених конструкторів для малювання ліній з вказаним кольором, шириною та пензликом. Клас SolidBrush використовується для постійного малювання з конкретним кольором. Наприкінці зображення експортується в формат файлу BMP. Наведений нижче уривок коду показує, як малювати форми ліній на поверхні зображення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}

## **Малювання еліпсів**
Приклад малювання еліпса є другою статтею у серії малювання форм. Ми використовуємо клас Graphics для малювання форми еліпса на поверхні зображення. Для демонстрації операції приклад створює нове зображення та малює форму еліпса на поверхні зображення, використовуючи метод DrawEllipse, викладений класом Graphics. Спочатку ми створимо об'єкт PsdImage, вказавши його висоту та ширину.

Після створення зображення ми створимо та ініціалізуємо об'єкт класу Graphics та встановимо фоновий колір зображення, використовуючи метод Clear класу Graphics. Метод DrawEllipse класу Graphics використовується для малювання форми еліпса на поверхні зображення, вказаної структурою обмежуючого прямокутника. Цей метод має кілька варіантів перегрузки, які приймають екземпляри класів Pen та Rectangle/RectangleF або пару координат, висоту та ширину як аргументи. Клас Pen визначає об'єкт, який використовується для малювання ліній, кривих та фігур. У класі Pen є кілька перегружених конструкторів для малювання ліній з вказаним кольором, шириною та пензликом. Клас Rectangle зберігає набір чотирьох цілих чисел, які представляють місце та розмір прямокутника. У класі Rectangle є кілька перегружених конструкторів для малювання структури прямокутника з вказаним розміром та місцем. Клас SolidBrush використовується для постійного малювання з конкретним кольором. Наприкінці зображення експортується в формат файлу BMP. Наведений нижче уривок коду показує, як малювати форму еліпса на поверхні зображення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

## **Малювання прямокутників**
У цьому прикладі ми намалюємо форму прямокутника на поверхні зображення. Для демонстрації операції приклад створює нове зображення та малює форму прямокутника на поверхні зображення, використовуючи метод DrawRectangle, викладений класом Graphics. Спочатку ми створимо об'єкт PsdImage, вказавши його висоту та ширину. Потім ми встановимо фоновий колір зображення з використанням методу Clear класу Graphics.

Метод DrawRectangle класу Graphics використовується для малювання форми прямокутника на поверхні зображення, вказаної структурою прямокутника. Цей метод має кілька варіантів перегрузки, які приймають екземпляри класів Pen та Rectangle/RectangleF або пару координат, ширину та висоту як аргументи. Клас Rectangle зберігає набір чотирьох цілих чисел, які представляють місце та розмір прямокутника. У класі Rectangle є кілька перегружених конструкторів для малювання структури прямокутника з вказаним розміром та місцем. Наприкінці зображення експортується в формат файлу BMP. Наведений нижче уривок коду показує, як малювати форму прямокутника на поверхні зображення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}

## **Малювання дуги**
У цьому випуску серії малювання форм ми намалюємо форму дуги на поверхні зображення. Ми використаємо метод DrawArc класу Graphics, щоб продемонструвати операцію на зображенні BMP. Спочатку ми створимо об'єкт PsdImage, вказавши його висоту та ширину. Після створення зображення ми використовуємо метод Clear, викладений класом Graphics, щоб встановити його фоновий колір. 

Метод DrawArc класу Graphics використовується для малювання форми дуги на поверхні зображення. DrawArc представляє частину еліпса, вказаного структурою прямокутника або парою координат. Цей метод має кілька варіантів перегрузки, які приймають екземпляри класів Pen та Rectangle / RectangleF або пару координат, ширину та висоту як аргументи. Наприкінці зображення експортується в формат файлу BMP. Наведений нижче уривок коду показує, як малювати форму дуги на поверхні зображення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

## **Малювання кривої Без'є**
У цьому прикладі використовується клас Graphics для малювання форми кривої Без'є на поверхні зображення. Для демонстрації операції приклад створює нове зображення та малює форму кривої Без'є на поверхні зображення, використовуючи метод DrawBezier, викладений класом Graphics. Спочатку ми створимо об'єкт PsdImage, вказавши його висоту та ширину. Після створення зображення ми використаємо метод Clear, викладений класом Graphics, щоб встановити його фоновий колір.

Метод DrawBezier класу Graphics використовується для малювання форми кривої Без'є на поверхні зображення, визначеної чотирма структурами Point. Цей метод має кілька варіантів перегрузки, які приймають екземпляри класу Pen та чотири впорядковані пари координат або чотири структури Point/PointF або масив структур Point/PointF. Клас Pen визначає об'єкт, що використовується для малювання ліній, кривих та фігур. У класі Pen є кілька перегружених конструкторів для малювання ліній з вказаним кольором, шириною та пензликом. Наприкінці зображення експортується в формат файлу BMP. Наведений нижче уривок коду показує, як малювати форму кривої Без'є на поверхні зображення.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

## **Малювання зображень за допомогою основного функціоналу**
Aspose.PSD - це бібліотека, яка пропонує багато цінних функцій, включаючи створення зображень з нуля. Малюйте за допомогою основного функціоналу, такого як маніпулювання інформацією про бітове зображення або використання розширених функцій, таких як Graphics та GraphicsPath для малювання форм на поверхні зображення за допомогою різних пензликів та пера. За допомогою класу RasterImage Aspose.PSD ви можете отримати інформацію про пікселі ділянки зображення та маніпулювати нею. Клас RasterImage містить весь основний функціонал малювання, такий як отримання та встановлення пікселів та інші методи для маніпулювання зображенням. Створіть нове зображення, використовуючи один із методів, описаних у створенні файлів, та присвойте його екземпляру класу RasterImage. Використовуйте метод LoadPixels класу RasterImage для отримання інформації про пікселі ділянки зображення. Після того як у вас є масив пікселів, ви можете маніпулювати ним, наприклад, змінюючи колір кожного пікселя. Після маніпулювання інформацією про пікселі встановіть її назад у бажану область зображення з використанням методу SavePixels класу RasterImage. Наведений нижче уривок коду показує, як малювати зображення за допомогою основного функціоналу.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
