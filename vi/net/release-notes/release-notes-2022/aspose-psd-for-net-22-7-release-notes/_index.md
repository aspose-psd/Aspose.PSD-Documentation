---
title: Ghi chú phát hành Aspose.PSD cho .NET 22.7
type: docs
weight: 60
url: /vi/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú phát hành cho [Aspose.PSD cho .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-482|Hỗ trợ của Tài nguyên Phần cắt Hình ảnh #4000-4999# Plugin(s)|Tính năng|
|PSDNET-875|Một ngoại lệ chưa xử lý loại "System.OutOfMemoryException" xuất hiện trong Aspose.PSD.dll|Lỗi|
|PSDNET-1050|Sau khi xuất tệp PSD, kết quả lớn hơn nhiều so với tệp nguồn|Lỗi|
|PSDNET-1083|Dữ liệu phân tích không chính xác cho XmpResource|Lỗi|
|PSDNET-1205|Sau khi xuất, kích thước các tệp PSD với các thư mục con đã tăng lên|Lỗi|


## **Thay đổi API công khai**
# **API được thêm vào:**
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


# **API đã bị xóa:**
- Không có


## **Ví dụ về cách sử dụng:**

**PSDNET-482. Hỗ trợ của Tài nguyên Phần cắt Hình ảnh #4000-4999# Plugin(s)**

{{< highlight csharp >}}
// Mã sau biểu diễn cách thiết lập/cập nhật thời gian trễ trong khung dòng thời gian của dữ liệu hoạt ảnh.
string tệpNguồn = "3_animated.psd";
string kếtQuảPsd = "output_3_animated.psd";

T TìmCấuTrúc<T>(IEnumerable<OSTypeStructure> cấuTrúcs, string keyName) where T : OSTypeStructure
{
    foreach (var cấuTrúc in cấuTrúcs)
    {
        if (cấuTrúc.KeyName.ClassName == keyName)
        {
            return cấuTrúc as T;
        }
    }

    return null;
}

OSTypeStructure[] ThêmHoặcThayThếCấuTrúc(IEnumerable<OSTypeStructure> cấuTrúcs, OSTypeStructure cấuTrúcMới)
{
    List<OSTypeStructure> danhSáchCấuTrúcs = new List<OSTypeStructure>(cấuTrúcs);

    for (int i = 0; i < danhSáchCấuTrúcs.Count; i++)
    {
        OSTypeStructure cấuTrúc = danhSáchCấuTrúcs[i];
        if (cấuTrúc.KeyName.ClassName == cấuTrúcMới.KeyName.ClassName)
        {
            danhSáchCấuTrúcs.RemoveAt(i);
            break;
        }
    }

    danhSáchCấuTrúcs.Add(cấuTrúcMới);

    return danhSáchCấuTrúcs.ToArray();
}

using (PsdImage hìnhẢnh = (PsdImage)Image.Load(tệpNguồn))
{
    foreach (var tàiNguyênHìnhẢnh in hìnhẢnh.ImageResources)
    {
        if (tàiNguyênHìnhẢnh is AnimatedDataSectionResource)
        {
            var dữLiệuHoạtHình =
            (AnimatedDataSectionStructure) (tàiNguyênHìnhẢnh as AnimatedDataSectionResource).AnimatedDataSection;
            var danhSáchKhung = TìmCấuTrúc<ListStructure>(dữLiệuHoạtHình.Items, "FrIn");

            var khung1 = (DescriptorStructure)danhSáchKhung.Types[1];

            // Tạo bản ghi thời gian trễ khung với giá trị 100 centi-giây tương đương với 1 giây.
            var thờiGianTrễKhung = new IntegerStructure(new ClassID("FrDl"));
            thờiGianTrễKhung.Value = 100; // thiết lập thời gian trong centi-giây.

            khung1.CấuTrúcs = ThêmHoặcThayThếCấuTrúc(khung1.CấuTrúcs, thờiGianTrễKhung);

            break;
        }
    }

    hìnhẢnh.Save(kếtQuảPsd);
}
{{< /highlight >}}

**PSDNET-875. Một ngoại lệ chưa xử lý loại "System.OutOfMemoryException" xuất hiện trong Aspose.PSD.dll**

{{< highlight csharp >}}
string tệpNguồn = "001-.psd";
string đườngDẫnJpg = "T_0003.jpg";
string đườngDẫnKếtQuả = "output_newPsd.psd";

using (var ảnh = (PsdImage)Image.Load(tệpNguồn))
{
    using (FileStream fs = new FileStream(đườngDẫnJpg, FileMode.Open))
    {
        var lớpMới = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        lớpMới.DisplayName = "LớpMới";

        ảnh.AddLayer(lớpMới);

        ảnh.Save(đườngDẫnKếtQuả, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Sau khi xuất tệp PSD, kết quả lớn hơn nhiều so với tệp nguồn**

{{< highlight csharp >}}
string nguồn = "ShimadzuLetterhead100.psd";
string kếtQuả = "output.psd";
using (var ảnh = (PsdImage)Image.Load(nguồn))
{
    ảnh.Save(kếtQuả);
}

double kíchThướcKếtQuảMb = new FileInfo(kếtQuả).Length / 1024d / 1024d;
if (kíchThướcKếtQuảMb > 6)
{
    throw new Exception("Tệp kết quả lớn hơn nên phải.");
}
{{< /highlight >}}

**PSDNET-1083. Dữ liệu phân tích không chính xác cho XmpResource**

{{< highlight csharp >}}
string đườngDẫnHìnhPsdNhập = @"input.psd";
string đườngDẫnHìnhPsdĐãLưu = @"saved.psd";

bool làBanĐầuChứa = false;
bool làĐãLưuChứa = false;

// Tìm khóa XMP con trong tệp đầu vào
using (PsdImage ảnh = (PsdImage)Image.Load(đườngDẫnHìnhPsdNhập))
{
    foreach (var gói in ảnh.XmpData.Packages)
    {
        foreach (var baoGồm trong gói)
        {
            if (baoGồm.Value is XmpArray)
            {
                XmpArray mảngXmp = (XmpArray)baoGồm.Value;

                string giáTrịXml = mảngXmp.GetXmlValue();

                if (giáTrịXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    làBanĐầuChứa = true;
                    break;
                }
            }
        }

        if (làBanĐầuChứa)
        {
            break;
        }
    }
    ảnh.Save(đườngDẫnHìnhPsdĐãLưu);
}

// Tìm khóa XMP con trong tệp đã lưu
using (PsdImage ảnh = (PsdImage)Image.Load(đườngDẫnHìnhPsdĐãLưu))
{
    foreach (var gói in ảnh.XmpData.Packages)
    {
        foreach (var baoGồm trong gói)
        {
            if (baoGồm.Value is XmpArray)
            {
                XmpArray mảngXmp = (XmpArray)baoGồm.Value;

                string giáTrịXml = mảngXmp.GetXmlValue();

                if (giáTrịXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    làĐãLưuChứa = true;
                    break;
                }
            }
        }

        if (làĐãLưuChứa)
        {
            break;
        }
    }
    ảnh.Save(đườngDẫnHìnhPsdĐãLưu);
}

if (làBanĐầuChứa && làĐãLưuChứa)
{
    // Tất cả đều ổn!
}
else
{
    throw new Exception("Nó không hoạt động");
}
{{< /highlight >}}

**PSDNET-1205. Sau khi xuất, kích thước các tệp PSD với các thư mục con đã tăng lên**

{{< highlight csharp >}}
string[] tệpNguồn = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var tênTệp trong tệpNguồn)
{
    string đườngDẫnTệpNguồn = tênTệp;
    string đườngDẫnTệpKếtQuả = "output_" + tênTệp;

    using (PsdImage hìnhẢnh = (PsdImage)Image.Load(đườngDẫnTệpNguồn))
    {
        hìnhẢnh.Save(đườngDẫnTệpKếtQuả);
    }

    double kíchThướcKếtQuảMb = new FileInfo(đườngDẫnTệpKếtQuả).Length / 1024d / 1024d;
    if (kíchThướcKếtQuảMb > 1.9)
    {
        throw new Exception("Tệp kết quả lớn hơn nên phải.");
    }
}
{{< /highlight >}}
