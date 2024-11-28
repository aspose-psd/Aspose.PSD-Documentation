---
title: Note sulla pubblicazione di Aspose.PSD Adapters per .NET 24.4
type: docs
weight: 100
url: /it/net/adapters/aspose-psd-adapters-per-net-24-4-note-sulla-pubblicazione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla pubblicazione di [Aspose.PSD Adapters per .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                            | **Categoria** |
|:-----------|:------------------------------------------------------------------------|:------------|
| PSDNET-1985 | Pubblicazione iniziale di Aspose.PSD.Adapters.Imaging su Nuget          | Miglioramento |


## **Cambiamenti nell'API Pubblica**
# **API Aggiunte:**
- Nessuna

# **API Rimosse:**
- Nessuna

## **Esempi di utilizzo:**

Si prega di controllare la [pagina di documentazione di Aspose.PSD.Adapters](/psd/it/net/adapters)

**PSDNET-1985. Esempio più completo di utilizzo di Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Aggiungi l'abilitazione degli adattatori nella tua configurazione di inizializzazione
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// abilita inoltre gli Esportatori
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Per lavorare con gli adattatori hai bisogno delle Licenze Aspose.PSD e Adaptee
// Ecco come applicare la Licenza Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Ecco un esempio di come applicare la Licenza Adaptee per Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Poi puoi eseguire qualsiasi codice degli adattatori o delle librerie PSD o Imaging

// Dopo di ciò, tutti questi file possono essere aperti da Aspose.PSD senza alcun codice aggiuntivo, basta usare
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Dopo l'esecuzione di questo codice otterrai un file PSD creato da WEBP e potrai applicare qualsiasi filtro, livello e aggiustamento di Aspose.PSD, inclusa la trasformazione Warp.
}

// Puoi inoltre creare immagini Export Adaptees in formato PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Usa l'API Aspose.Imaging per modificare il file WEBP con funzionalità specifiche di Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Poi usa semplicemente il metodo ToPsdImage() e modifica il file come un PSD con funzionalità simili a Photoshop incluse le maschere, i filtri intelligenti e gli oggetti intelligenti.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Salva il file PSD finale utilizzando Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Se non hai bisogno di utilizzare gli adattatori forniti dai caricatori o dagli esportatori, basta disabilitarli
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
