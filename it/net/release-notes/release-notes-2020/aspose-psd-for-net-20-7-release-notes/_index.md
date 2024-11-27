---
title: Note sulla versione di Aspose.PSD for .NET 20.7
type: docs
weight: 60
url: /it/net/aspose-psd-for-net-20-7-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-673|Supporto di LnkE Resource|Funzionalità|
|PSDNET-392|Supporto di britResource (Risorsa del livello di regolazione luminosità/contrasto)|Funzionalità|
|PSDNET-629|Modifica del messaggio di eccezione al tentativo di aprire formati non supportati come un'immagine|Potenziamento|
|PSDNET-594|Impossibilità di salvare LayerMask|Baco|
|PSDNET-597|Se si salva il file PSD dopo la creazione di un nuovo Gruppo di livelli, si riceve un avviso di Photoshop all'apertura del file|Baco|
|PSDNET-618|Maschera di ritaglio non applicata alla cartella|Baco|
|PSDNET-625|Impossibile aprire il file con Aspose.PSD for .NET|Baco|
|PSDNET-650|Eccezione di salvataggio immagine durante la conversione di PSD in PDF|Baco|
|PSDNET-655|Operazione rop rende il percorso di ritaglio non valido nell'immagine PSD|Baco|
|PSDNET-662|Eccezione NullReference durante il tentativo di salvare un file PSD specifico con l'Effetto ombra|Baco|
|PSDNET-666|Aspose.PSD restituisce true su Image.CanLoad(pdfStream)|Baco|
|PSDNET-676|Livelli non si caricano correttamente nel PNG generato|Baco|
|PSDNET-677|Eccezione nell'accesso ai dati del testo|Baco|
|PSDNET-679|ImageSaveException durante il salvataggio del PSD|Baco|

## **Modifiche all'API pubblica**
# **API aggiuntive:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **API rimosse:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Esempi d'uso:**
**PSDNET-606. Supporto di LnkE Resource**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(actual, expected))
    {
        throw new FormatException(string.Format("Il valore attuale {0} non corrisponde al previsto {1}.", actual, expected));
    }
    
}

object[] Lnk2ResourceSupportCases = new object[]
{
    new object[]
    {
        "00af34a0-a90b-674d-a821-73ee508c5479",
        "rgb8_2x2.png",
        "png",
        string.Empty,
        0x53,
        0d,
        string.Empty,
        7,
        true,
        0x124L,
        0x74cL
    }
};
// Altri casi di supporto dei dati
{{< /highlight >}}
**PSDNET-201. Supporto per il progresso della conversione del documento**

{{< highlight csharp >}}
string sourceFilePath = "Mela.psd";
Stream outputStream = new MemoryStream();
ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)
{
    string message = string.Format(
        "{0} {1}: {2} su {3}",
        progressInfo.Description,
        progressInfo.EventType,
        progressInfo.Value,
        progressInfo.MaxValue);
    Console.WriteLine(message);
};
// Altri codici di supporto per la conversione del documento
{{< /highlight >}}

**PSDNET-386. Supporto di britResource (Risorsa del livello di regolazione luminosità/contrasto)**

{{< highlight csharp >}}
 /* Questo esempio dimostra come è possibile modificare programmaticamente la risorsa di luminosità/contrasto dell'immagine PSD - BritResource

   Questa è un'API di basso livello di Aspose.PSD. Si può utilizzare lo Strato di luminosità/contrasto attraverso la sua API, che sarà molto più facile, 

   ma la modifica diretta delle risorse di photoshop offre maggiore controllo sul contenuto del file PSD. */

string path = @"LuminositaContrastoPS6.psd";
string outputPath = @"LuminositaContrastoPS6_output.psd";
// Altri codici di supporto per la luminosità/contrasto
{{< /highlight >}}

**PSDNET-596. Gruppi di livelli con modalità di fusione non pass-through non vengono resi**

{{< highlight csharp >}}
 string sourceFilePath = "TestMascheraNormaleMascheraGruppo.psd";
string outputFilePath = "TestMascheraNormaleMascheraGruppo.png";
// Altri codici di supporto per i gruppi di livelli
{{< /highlight >}}

E così via per gli altri esempi e riferimenti forniti.