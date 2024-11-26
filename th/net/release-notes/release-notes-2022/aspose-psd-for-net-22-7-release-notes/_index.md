---
title: บันทึกการอัปเดต Aspose.PSD for .NET 22.7
type: คู่มือ
weight: 60
url: /th/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-482|การสนับสนุนของ Image Section Resource #4000-4999 แหล่งของปลั๊กอิน|คุณสมบัติ|
|PSDNET-875|An ข้อยกเว้นที่ไม่ถูกจัดการของชนิด "System.OutOfMemoryException" เกิดขึ้นใน Aspose.PSD.dll|บั๊ก|
|PSDNET-1050|หลังจากทำการส่งออกไฟล์ PSD ไฟล์ที่ผลลัพธ์ขนาดใหญ่กว่าไฟล์ต้นฉบับ|บั๊ก|
|PSDNET-1083|การวิเคราะห์ข้อมูลที่ไม่ถูกต้องสำหรับ XmpResource|บั๊ก|
|PSDNET-1205|หลังจากการส่งออก ขนาดของไฟล์ PSD ที่มีโฟลเดอร์ย่อยมีการเพิ่มขึ้น|บั๊ก|


## **การเปลี่ยนแปลง API สาธารณะ**
# **APIs ที่เพิ่มเข้ามา:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **APIs ที่ถูกนำออก:**
- None


## **ตัวอย่างการใช้:**

**PSDNET-482. การสนับสนุนของ Image Section Resource #4000-4999 แหล่งของปลั๊กอิน**

{{< highlight csharp >}}
// โค้ดต่อไปนี้แสดงถึงวิธีการตั้งค่า/อัปเดตเวลาหน่วยเวลาในกรอบไทม์ไลน์ของข้อมูลที่เคลื่อนไหว
string sourceFile = "3_animated.psd";
string outputPsd = "output_3_animated.psd";

T FindStructure<T>(IEnumerable<OSTypeStructure> structures, string keyName) where T : OSTypeStructure
{
    foreach (var structure in structures)
    {
        if (structure.KeyName.ClassName == keyName)
        {
            return structure as T;
        }
    }

    return null;
}

OSTypeStructure[] AddOrReplaceStructure(IEnumerable<OSTypeStructure> structures, OSTypeStructure newStructure)
{
    List<OSTypeStructure> listOfStructures = new List<OSTypeStructure>(structures);

    for (int i = 0; i < listOfStructures.Count; i++)
    {
        OSTypeStructure structure = listOfStructures[i];
        if (structure.KeyName.ClassName == newStructure.KeyName.ClassName)
        {
            listOfStructures.RemoveAt(i);
            break;
        }
    }

    listOfStructures.Add(newStructure);

    return listOfStructures.ToArray();
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    foreach (var imageResource in image.ImageResources)
    {
        if (imageResource is AnimatedDataSectionResource)
        {
            var animatedData =
            (AnimatedDataSectionStructure) (imageResource as AnimatedDataSectionResource).AnimatedDataSection;
            var framesList = FindStructure<ListStructure>(animatedData.Items, "FrIn");

            var frame1 = (DescriptorStructure)framesList.Types[1];

            // สร้างเรคอร์ดการชะลอเฟรมด้วยค่า 100 เซนตี้เซคอนด์ ที่เท่ากับ 1 วินาที
            var frameDelay = new IntegerStructure(new ClassID("FrDl"));
            frameDelay.Value = 100; // ตั้งค่าเวลาในเซนตี้เซคอนด์

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameDelay);

            break;
        }
    }

    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-875. An ข้อยกเว้นที่ไม่ถูกจัดการของชนิด "System.OutOfMemoryException" เกิดขึ้นใน Aspose.PSD.dll**

{{< highlight csharp >}}
string srcFile = "001-.psd";
string jpgFilePath = "T_0003.jpg";
string outputFilePath = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    using (FileStream fs = new FileStream(jpgFilePath, FileMode.Open))
    {
        var newLayer = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        newLayer.DisplayName = "NewLayer";

        im.AddLayer(newLayer);

        im.Save(outputFilePath, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. หลังจากทำการส่งออกไฟล์ PSD ไฟล์ที่ผลลัพธ์ขนาดใหญ่กว่าไฟล์ต้นฉบับ**

{{< highlight csharp >}}
string src = "ShimadzuLetterhead100.psd";
string output = "output.psd";
using (var img = (PsdImage)Image.Load(src))
{
    img.Save(output);
}

double outputSizeMb = new FileInfo(output).Length / 1024d / 1024d;
if (outputSizeMb > 6)
{
    throw new Exception("ไฟล์ผลลัพธ์ใหญ่กว่าที่ควรจะเป็น");
}
{{< /highlight >}}

**PSDNET-1083. การวิเคราะห์ข้อมูลที่ไม่ถูกต้องสำหรับ XmpResource**

{{< highlight csharp >}}
string inputPsdImagePath = @"input.psd";
string savedPsdImagePath = @"saved.psd";

bool isOriginalContain = false;
bool isSavedContain = false;

// ค้นหาคีย์ XMP ย่อ ในไฟล์นำเข้า
using (PsdImage img = (PsdImage)Image.Load(inputPsdImagePath))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string xmlValue = xmpArray.GetXmlValue();

                if (xmlValue.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    isOriginalContain = true;
                    break;
                }
            }
        }

        if (isOriginalContain)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

// ค้นหาคีย์ XMP ย่อในไฟล์ที่บันทึก
using (PsdImage img = (PsdImage)Image.Load(savedPsdImagePath))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string xmlValue = xmpArray.GetXmlValue();

                if (xmlValue.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    isSavedContain = true;
                    break;
                }
            }
        }

        if (isSavedContain)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

if (isOriginalContain && isSavedContain)
{
    // ทุกอย่างดี!
}
else
{
    throw new Exception("ไม่ทำงาน");
}
{{< /highlight >}}

**PSDNET-1205. หลังจากการส่งออก ขนาดของไฟล์ PSD ที่มีโฟลเดอร์ย่อยมีการเพิ่ม**

{{< highlight csharp >}}
string[] sourceFiles = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var fileName in sourceFiles)
{
    string sourceFilePath = fileName;
    string outputFilePath = "output_" + fileName;

    using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
    {
        image.Save(outputFilePath);
    }

    double outputSizeMb = new FileInfo(outputFilePath).Length / 1024d / 1024d;
    if (outputSizeMb > 1.9)
    {
        throw new Exception("ไฟล์ผลลัพธ์ใหญ่กว่าที่ควรจะเป็น");
    }
}
{{< /highlight >}}
