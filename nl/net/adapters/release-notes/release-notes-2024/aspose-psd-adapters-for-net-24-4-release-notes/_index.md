---
title: Aspose.PSD Adapters for .NET 24.4 - Release Notes
type: docs
weight: 100
url: /nl/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD Adapters voor .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                    | **Categorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Eerste publicatie van Aspose.PSD.Adapters.Imaging op Nuget         | Uitbreiding |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

Bekijk alstublieft de [Aspose.PSD.Adapters documentatiepagina](/psd/nl/net/adapters)

**PSDNET-1985. Meest volledige voorbeeld van het gebruik van Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Voeg het inschakelen van adapters toe in uw configuratie
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// Schakel bovendien Exporters in
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Om met adapters te werken, heeft u zowel Aspose.PSD als adaptee-licenties nodig
// Zo past u de Aspose.PSD Licentie toe
var licentie = new Aspose.PSD.License();
licentie.SetLicense(@"Aspose.PSD.NET.lic");

// Hier is een voorbeeld van het toepassen van de Adaptee License voor Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Vervolgens kunt u elke code van adapters of PSD of Imaging-bibliotheek uitvoeren

// Hierna kunnen al deze bestanden worden geopend door Aspose.PSD zonder extra code, gebruik gewoon
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Na uitvoering van deze code krijgt u het PSD-bestand gemaakt van WEBP en kunt u eventuele Aspose.PSD filters, lagen en aanpassingen toepassen, inclusief Warp-transformatie
}

// U kunt bovendien Export Adaptees' Images naar PSD-indeling maken
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Gebruik Aspose.Imaging API om WEBP-bestand te bewerken met Imaging-specifieke functies
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Gebruik dan gewoon de ToPsdImage() methode en bewerk het bestand als PSD met Photoshop-achtige functies inclusief lagen, slimme filters en slimme objecten.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Wat tekst", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Sla het eindresultaat op als PSD-bestand met behulp van Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Als u geen gebruik wilt maken van de Loaders of Exporters die door Adapters worden geleverd, schakel deze dan uit
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
