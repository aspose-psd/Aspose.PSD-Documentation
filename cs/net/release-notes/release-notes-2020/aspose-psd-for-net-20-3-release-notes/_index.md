---
title: Aspose.PSD pro .NET 20.3 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/aspose-psd-pro-net-20-3-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-188|Podpora .Net Core|Funkce|
|PSDNET-523|Konverze souborů Adobe Illustrator do formátu PDF|Funkce|
|PSDNET-212|Přidání schopnosti zobrazit různé styly v jedné textové vrstvě|Funkce|
|PSDNET-144|Podpora vrstvy úpravy černé a bílé|Funkce|
|PSDNET-233|Přidání podpory exportu formátu AI (Verze 8) do jiných formátů|Funkce|
|PSDNET-540|Podpora zpracování průchodného režimu míchání (Použito pouze pro skupinu vrstev)|Funkce|
|PSDNET-539|Výjimka: Chyba při načítání obrázku s prázdnými Unicode názvy alfa zdroje|Chyba|
|PSDNET-541|Nesprávný výstup po změně viditelnosti vrstevné skupiny|Chyba|
|PSDNET-516|Výjimka při načítání obrázku PSD: Část barev (DropShadow Resource) musí obsahovat 3 složky barev pro RGB nebo 4 složky barev pro CMYK|Chyba|
|PSDNET-536|Výjimka v případě pokusu kreslit na nově vytvořenou vrstvu, pokud je použita jednoduchá verze konstruktoru|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**

- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)

# **Odstraněná API:**
- Žádné

## **Příklady použití:**
**PSDNET-523. Konverze souborů Adobe Illustrator do formátu PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Přidání schopnosti zobrazit různé styly v jedné textové vrstvě**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // Úprava textového stylu "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // Úprava textového stylu "2\r"

    newPortions[2].Style.FauxBold = true; // Úprava textového stylu "Bold"

    newPortions[3].Style.FauxItalic = true; // Úprava textového stylu "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // Úprava textového stylu "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // Úprava textového stylu "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Přidání podpory exportu formátu AI (Verze 8) do jiných formátů**

{{< highlight java >}}

 // Příklad exportu souboru AI do formátu PSD a PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Podpora zpracování průchodného režimu míchání (Použito pouze pro skupinu vrstev)**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Není zde 23. vrstva.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "23. vrstva není vrstvou skupiny.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Název 23. vrstvy není 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Vrstva AdjustmentGroup by měla mít režim míchání 'průchod'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Aktualizace textové vrstvy vyvolává výjimku**

{{< highlight java >}}

 // Aktualizace textové vrstvy vyvolává výjimku

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Uložení obrázku PSD po operaci RotateFlip produkuje poškozený soubor, který nelze otevřít.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Mělo by být provedeno bez výjimek

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Nic nedělej

}

{{< /highlight >}}

**PSDNET-539. Výjimka: Chyba při načítání obrázku s prázdnými Unicode názvy alfa zdroje**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Zde bychom neměli dostat žádné výjimky

{

    // nic nedělej

}

{{< /highlight >}}

**PSDNET-541. Nesprávný výstup po změně viditelnosti vrstevné skupiny**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// provádění změn ve jménech vrstev a uložení

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Vypnout vše uvnitř skupiny

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Výjimka při načítání obrázku PSD: Část barev (DropShadow Resource) musí obsahovat 3 složky barev pro RGB nebo 4 složky barev pro CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Zde bychom neměli dostat žádné výjimky

{

    // nic nedělej

}

{{< /highlight >}}

**PSDNET-536. Výjimka při pokusu o kreslení na nově vytvořenou vrstvu, pokud je použita jednoduchá verze konstruktoru**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // nakreslit obdélník s perem

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // nakreslit další obdélník se Solid Brush v modré barvě

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}
