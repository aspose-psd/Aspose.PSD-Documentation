---
title: Використання PSD-файлів як шаблонів для автоматизації - Випадок візиток
type: docs
weight: 10
url: /uk/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **Огляд**
Ця стаття описує часто використовувані випадки, коли вам потрібно оновлювати деякі шари в [PSD-файлі](https://wiki.fileformat.com/image/psd/) програмно, де PSD/PSB-файл має відому структуру типового шаблону. Це може бути використано для створення великої кількості візиток для різних осіб (Випадок візиток). Або вам потрібно перекласти файл PSD на різні мови заміняючи в ньому графічний матеріал.

Після прочитання цієї статті ви будете знати, як зробити це:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)

## **Простий випадок**
Наприклад, у вас є деякий PSD-шаблон з відомими назвами шарів. Отже, вам потрібно змінити, оновити або замінити шар PSD через C#. Спочатку вам потрібно відкрити файл шаблону за допомогою Aspose.PSD.

Як відкрити файл PSD за допомогою C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Потім нам потрібно знайти шар, який ми хочемо замінити за його назвою. Ось проста реалізація для цього.

Як знайти шар у файлі PSD за його назвою

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



Коли шар знайдено, ми можемо оновити його звичайним способом, використовуючи [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Як малювати на графіці шара PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

У цьому випадку ми малюємо нове завантажене [PNG-зображення](https://wiki.fileformat.com/image/png/) на існуючий шар PSD, тому старі дані будуть втрачені в новому файлі.

Але якщо нам також потрібно оновити текст? Процес буде схожим. Знайдіть [Текстовий Шар](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) за його ім'ям, тоді ми програмно [оновлюємо Текстовий Шар у Файлі Photoshop](/psd/uk/net/render-text-with-different-colors-in-text-layer/) за допомогою C#.

Як оновити Текстовий Шар в Photoshop за допомогою C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



Наприкінці нам потрібно зберегти наші зміни:

Як зберегти змінений файл PSD за допомогою [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



Результуюче зображення:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **Складний випадок із додатковими функціями**
Вище ми показали найпростіший спосіб заміни зображення в шарі PSD-файлу.

Проте Aspose.PSD може пропонувати складніші додаткові функції, такі як додавання нового шару, видалення старих шарів та оновлення текстового шару з використанням різних стилів у багатолучевому тексті.

Ми можемо знайти [Шар](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer), який ми хочемо замінити, після чого знайти його індекс у списку Шарів, видалити його і вставити новий Шар після створення його з [Файлу Jpeg](https://wiki.fileformat.com/image/jpeg/) на те саме місце.

Створіть новий шар з файлу та вставте його в зображення PSD з використанням [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



У кінцевому коді цього файлу ми виправляємо позицію шару та зберігаємо новий масив Шарів у зображенні Psd.

Як скопіювати властивості шару [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



І на завершення, нам потрібно оновити текстові шари в існуючому зображенні PSD за допомогою C#. Aspose.PSD підтримує [оновлення Текстового Шару частинами](/psd/uk/net/working-with-text-layers/). Кожна [частина тексту](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) має унікальну комбінацію властивостей Стилю та Абзацу.

Як скопіювати властивості шару [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



В результаті ми змінили шаблон PSD за допомогою коду з новим Шаром з файлу Jpeg, Png, J2k, Bmp, Gif або Tiff та багатолучевим [текстом з різними стилями](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) в кожному рядку.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
