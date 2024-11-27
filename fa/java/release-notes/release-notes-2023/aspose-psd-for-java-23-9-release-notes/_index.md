---
title: دستاوردهای انتشار Aspose.PSD برای جاوا 23.9
type: مستندات
weight: 40
url: /fa/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} این صفحه اطلاعات انتشار را برای [Aspose.PSD برای جاوا 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) شامل می‌شود. {{% /alert %}}

| **کلید**    | **خلاصه**                                                                                                                         | **دسته‌بندی** |
|:------------|:------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | پیاده‌سازی ایجاد ماسک برای لایه‌های تنظیم جدید                                                                                   |    قابلیت   |
| PSDJAVA-528 | اضافه کردن پشتیبانی از لایه‌های مختصر شده به عنوان گزینه ادغام گروهی                                                               |    قابلیت   |
| PSDJAVA-529 | فایل PSD با حالت رنگی 16 بیت ماسک را برای لایه‌های تنظیم اعمال نمی‌کند                                                             |      باگ     |
| PSDJAVA-530 | نادرست نمایش پرانتزها در لایه متن                                                                                                |      باگ     |
| PSDJAVA-531 | امکان بروزرسانی استایل‌ها در لایه‌های متن وجود ندارد                                                                             |      باگ     |
| PSDJAVA-532 | بعد از صدور فایل PSD با CMYK رنگ‌ها در PSD صادر شده شکسته می‌شوند                                                                |      باگ     |
| PSDJAVA-533 | فایل خاص PSB استثنا "مستطیل منطق پردازش مشترکی ندارد" پرتاب می‌کند                                                             |      باگ     |
| PSDJAVA-534 | بارگذاری تصویر ناموفق بود. OverflowException: Arithmetic operation resulted in an overflow.                                        |      باگ     |

## **تغییرات API عمومی**
# **API‌های اضافه شده:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **API‌های حذف شده:**

- هیچکدام

## **مثال‌های استفاده:**

**PSDJAVA-527. پیاده‌سازی ایجاد ماسک برای لایه‌های تنظیم جدید**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "اشکال در برابری اشیاء.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. اضافه کردن پشتیبانی از لایه‌های مختصر شده به عنوان گزینه ادغام گروهی**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

(سایر موارد به این فایل اضافه خواهد شد)
