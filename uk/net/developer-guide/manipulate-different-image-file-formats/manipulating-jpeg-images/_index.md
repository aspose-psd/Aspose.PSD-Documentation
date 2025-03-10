---
title: Обробка зображень у форматі JPEG
type: docs
weight: 30
url: /uk/net/manipulating-jpeg-images/
---

## **Використання класу ExifData для зчитування та зміни тегів Jpeg EXIF**
Майже всі цифрові камери (включаючи смартфони), сканери та інші системи, що обробляють зображення, зберігають зображення з інформацією EXIF (Exchangeable Image File). Налаштування камери та інформація про сцену записуються камерою у файл зображення. Дані EXIF також включають час дії діафрагми, дату та час, коли було зроблено фото, фокусну відстань, компенсацію експозиції, патерн вимірювання та, якщо використовувався спалах. API Aspose.Imaging зробив можливим видобування інформації EXIF з даного зображення дуже простим та простим способом. Розробники також можуть записувати дані EXIF до зображень або модифікувати існуючу інформацію з урахуванням їх вимог. Aspose.PSD надав клас [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) для зчитування, запису та модифікації даних EXIF, в той час як простір імен [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) містить відповідні переліки, що використовуються в процесі.
### **Зчитування даних EXIF**
API Aspose.PSD надає можливість зчитувати дані EXIF з даного зображення. Нижче наведені кроки ілюструють використання класу ExifData для зчитування інформації EXIF з зображення.

- Завантажте зображення PSD за допомогою методу завантаження.
- Знайдіть мініатюру Jpeg серед ресурсів PSD.
- Витягніть екземпляр класу ExifData.

Отримайте необхідну інформацію та виведіть її в консоль.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}

За потреби розробники також можуть отримувати конкретну інформацію за допомогою наступного фрагмента коду.
....


