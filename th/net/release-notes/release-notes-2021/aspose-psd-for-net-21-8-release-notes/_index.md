---
title: บันทึกการอัปเดต Aspose.PSD for .NET 21.8
type: สารบัญ
weight: 50
url: /th/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-698|สนับสนุนวิธีการบีบอัด ZipWithPrediction|คุณลักษณะ|
|PSDNET-663|ระยะช่องว่างข้อความไม่ถูกต้องใน PSD ที่สร้างขึ้น|ข้อผิดพลาด|
|PSDNET-685|ข้อยกเว้นในการบันทึก PSD|ข้อผิดพลาด|
|PSDNET-927|ระยะห่างไม่ถูกต้องระหว่างบรรทัดและสัญลักษณ์ใน Aspose.PSD เมื่อเราใช้โดยไม่มีใบอนุญาต|ข้อผิดพลาด|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API เพิ่มเติม:**
- ไม่มี

# **API ที่ถูกลบออก:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-663. ระยะช่องว่างข้อความไม่ถูกต้องใน PSD ที่สร้างขึ้น**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. ข้อยกเว้นในการบันทึก PSD**

{{< highlight csharp >}}
            string sourceFileName = "File.psd";
            string outputFileName = "File2.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                var layer1 = (TextLayer)image.Layers[1];
                layer1.TextData.UpdateLayerData();

                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-698. สนับสนุนวิธีการบีบอัด ZipWithPrediction**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";

            string outputPng = "output.png";
            string outputRaw = "out_Raw.psd";
            string outputZip = "out_Zip.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(outputPng, new PngOptions());

                image.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. ระยะห่างไม่ถูกต้องระหว่างบรรทัดและสัญลักษณ์ใน Aspose.PSD เมื่อเราใช้โดยไม่มีใบอนุญาต**

{{< highlight csharp >}}
            bool[] licenseStates = new bool[] { false, true };
            for (int i = 0; i < licenseStates.Length; i++)
            {
                bool testLicense = licenseStates[i];
                if (testLicense)
                {
                    License license = new License();
                    license.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string sourceFile = "psdnetTest927.psd";
                string outputFile = "out_" + testLicense.ToString() + "_psdnetTest927.png";

                using (var image = (PsdImage)Image.Load(sourceFile))
                {
                    image.Save(outputFile, new PngOptions());
                }
            }
{{< /highlight >}}
