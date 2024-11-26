---
title: Notatki wydania Aspose.PSD Adapters dla .NET 24.4
type: docs
weight: 100
url: /pl/net/adapters/aspose-psd-adapters-dla-net-24-4-notatki-wydania
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD Adapters dla .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                      | **Kategoria** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Pierwsze opublikowanie Aspose.PSD.Adapters.Imaging do Nuget          | Usprawnienie |


## **Zmiany w API publicznym**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

Proszę sprawdzić [stronę dokumentacji Aspose.PSD.Adapters](/pl/psd/net/adapters)

**PSDNET-1985. Najbardziej kompletny przykład korzystania z Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Dodaj włączenie adapterów w swojej konfiguracji początkowej
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// dodatkowo włącz eksporterów
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Aby pracować z adapterami, potrzebujesz licencje Aspose.PSD i adaptee
// Oto jak zastosować licencję Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Oto przykład zastosowania licencji Adaptee dla Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Następnie możesz uruchomić dowolny kod adapterów lub biblioteky PSD lub Imaging

// Po tym wszystkie te pliki mogą być otwarte przez Aspose.PSD bez żadnego dodatkowego kodu, wystarczy
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Po wykonaniu tego kodu otrzymasz plik PSD utworzony z WEBP i możesz zastosować dowolne filtry Aspose.PSD, warstwy i dostosowania, w tym transformację zakrzywienia
}

// Dodatkowo możesz tworzyć obrazy eksporterów w formacie PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Użyj interfejsu API Aspose.Imaging do edycji pliku WEBP z funkcjami specyficznymi dla obrazowania
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Następnie wystarczy użyć metody ToPsdImage() i edytować plik jak PSD ze funkcjami przypominającymi Photoshopa, w tym warstwy, inteligentne filtry i inteligentne obiekty.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Jakiś tekst", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Zapisz ostateczny plik PSD za pomocą Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Jeśli nie potrzebujesz korzystać z dostarczanych przez adapterów modułów wczytywania i eksportu, po prostu je wyłącz
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
