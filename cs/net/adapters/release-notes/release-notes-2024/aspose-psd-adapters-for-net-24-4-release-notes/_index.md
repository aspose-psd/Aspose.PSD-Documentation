---
title: Aspose.PSD Adaptéry pro .NET 24.4 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/adapters/aspose-psd-adapters-pro-net-24-4-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD Adaptéry pro .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                          | **Kategorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Počáteční publikování Aspose.PSD.Adapters.Imaging na Nuget            | Vylepšení |


## **Změny ve veřejném API**
# **Přidaná API:**
- žádné

# **Odstraněné API:**
- žádné

## **Příklady použití:**

Prosím zkontrolujte [stránku dokumentace Aspose.PSD Adaptérů](/psd/cs/net/adapters)

**PSDNET-1985. Nejúplnější příklad použití Aspose.PSD Adaptérů**

{{< highlight csharp >}}
// Přidání povolení adaptérů do vaší počáteční konfigurace 
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// dodatečně povolení Exportérů
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Pro práci s adaptéry potřebujete jak Licenci od Aspose.PSD, tak Licenci od adaptee
// Zde je, jak použít Licenci od Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Zde je příklad použití Licenci od Adaptee pro Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Poté můžete spustit jakýkoli kód adaptérů nebo SDK Aspose.PSD nebo Imaging

// Poté můžete otevřít jakýkoli z těchto souborů pomocí Aspose.PSD bez dalšího kódu pouze použijte
using (var img = Aspose.PSD.Image.Load("NějakýSoubor.Webp")) 
{
    // Po provedení tohoto kódu dostanete soubor PSD vytvořený z WEBP a můžete aplikovat jakékoli filtry, vrstvy a úpravy Aspose.PSD včetně transformace deformace
}

// Dodatečně můžete vytvářet exportní adaptéry obrazů do formátu PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Použijte Aspose.Imaging API k úpravám souboru WEBP s funkcemi specifickými pro obrazové zpracování
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Pak jednoduše použijte metodu ToPsdImage() a upravte soubor jako PSD s funkcemi podobnými Photoshopu včetně vrstev, chytrých filtrů a chytrých objektů.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Nějaký text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Uložte finální soubor PSD pomocí Aspose.PSD
        psdImage.Save("vystup.psd");
    }
}

// Pokud nepotřebujete používat poskytované Načítadla nebo Exportéry adaptérů, jednoduše je zakážete
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
