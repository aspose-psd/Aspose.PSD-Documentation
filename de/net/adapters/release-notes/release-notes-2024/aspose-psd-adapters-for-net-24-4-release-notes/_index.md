---
title: Aspose.PSD-Adapter für .NET 24.4 - Versionshinweise
type: docs
weight: 100
url: /de/net/adapters/aspose-psd-adapter-fur-net-24-4-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD-Adapter für .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                  | **Kategorie** |
|:-------------|:-------------------------------------------------------------------|:------------|
| PSDNET-1985  | Erstveröffentlichung von Aspose.PSD.Adapters.Imaging zu Nuget      | Verbesserung |

## **Änderungen in der öffentlichen API**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine

## **Verwendungsbeispiele:**

Bitte überprüfen Sie die [Aspose.PSD-Adapter-Dokumentationsseite](/psd/de/net/adapters)

**PSDNET-1985. Vollständigstes Beispiel zur Verwendung von Aspose.PSD-Adaptern**

{{< highlight csharp >}}
// Fügen Sie das Aktivieren von Adaptern in Ihrer Init-Konfiguration hinzu
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// Aktivieren Sie zusätzlich Exportierer
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Um mit Adaptern zu arbeiten, benötigen Sie Lizenzen sowohl für Aspose.PSD als auch für den konvertierten Datenträger (Adaptee)
// So wenden Sie die Aspose.PSD-Lizenz an
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Hier ein Beispiel, wie die Adaptee-Lizenz für Aspose.Imaging angewendet wird
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Danach können Sie beliebigen Code von Adaptern oder PSD- oder Imaging-Bibliotheken ausführen

// Anschließend können all diese Dateien von Aspose.PSD geöffnet werden, ohne dass zusätzlicher Code erforderlich ist, verwenden Sie einfach
using (var img = Aspose.PSD.Image.Load("EinigeDatei.Webp")) 
{
    // Nach Ausführung dieses Codes erhalten Sie die PSD-Datei, die aus WEBP erstellt wurde, und können beliebige Aspose.PSD-Filter, Ebenen und Anpassungen einschließlich Warp-Transformation anwenden
}

// Sie können außerdem Export-Adaptees-Bilder im PSD-Format erstellen
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Verwenden Sie die Aspose.Imaging-API, um die WEBP-Datei mit Imaging-spezifischen Funktionen zu bearbeiten
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Verwenden Sie dann einfach die Methode ToPsdImage() und bearbeiten Sie die Datei wie PSD mit Photoshop-ähnlichen Funktionen, einschließlich Ebenen, Smartfiltern und Smartobjekten
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Einiger Text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Speichern Sie die endgültige PSD-Datei mit Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Wenn Sie die von den Adaptern bereitgestellten Loader oder Exportierer nicht verwenden müssen, deaktivieren Sie sie einfach
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
