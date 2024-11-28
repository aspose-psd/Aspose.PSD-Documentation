---
title: Note sulla versione di Aspose.PSD per .NET 24.4
type: docs
weight: 90
url: /it/net/aspose-psd-per-net-24-4-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**   | **Sommario**                                            | **Categoria** |
|:------------|:-------------------------------------------------------|:-------------|
| PSDNET-1871 | [Formato AI] Aggiunta gestione delle risorse XObjectForm | Funzionalità |
| PSDNET-1961 | Aggiunto Costruttore per lo ShapeLayer                  | Funzionalità |
| PSDNET-1879 | Correzione della conversione del file Psd da RGB a CMYK | Bug          |
| PSDNET-1966 | Specifico file PSD non può essere esportato utilizzando Aspose.PSD | Bug          |

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **API Rimosse:**
- Nessuna

## **Esempi d'uso:**

**PSDNET-1871. [Formato AI] Aggiunta gestione delle risorse XObjectForm**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "esempio.ai");
string percorsoOutputFile = Path.Combine(cartellaOutput, "esempio.png");

using (AiImage immagine = (AiImage)Image.Load(fileSorgente))
{
    immagine.Save(percorsoOutputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. Correzione della conversione del file Psd da RGB a CMYK**

{{< highlight csharp >}}
// Verifica che il file psd convertito in CMYK + RLE 4 canali dal file psd in RGB + RLE 4 canali, abbia davvero 4 canali
// e HasTransparencyData == false.

string fileSorgente = Path.Combine(cartellaBase, "rana_nosymb.psd");
string outputFile = Path.Combine(cartellaOutput, "rana_nosymb_output.psd");

using (PsdImage immaginePsd = (PsdImage)Image.Load(fileSorgente))
{
    immaginePsd.HasTransparencyData = false;

    PsdOptions opzioniPsd = new PsdOptions(immaginePsd)
    {
        ColorMode = ColorModes.Cmyk,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
    };

    immaginePsd.Save(outputFile, opzioniPsd);
}

using (PsdImage immaginePsd = (PsdImage)Image.Load(outputFile))
{
    AssertAreEqual(false, immaginePsd.HasTransparencyData);
    AssertAreEqual((ushort)4, immaginePsd.Layers[0].ChannelsCount);
}

void AssertAreEqual(object atteso, object effettivo, string messaggio = null)
{
    if (!object.Equals(atteso, effettivo))
    {
        throw new Exception(messaggio ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1961. Aggiunto Costruttore per lo ShapeLayer**

{{< highlight csharp >}}
string outputFile = Path.Combine(cartellaOutput, "AggiungiShapeLayer_output.psd");

const int ImgToPsdRatio = 256 * 65535;

using (PsdImage nuovoPsd = new PsdImage(600, 400))
{
    ShapeLayer layer = nuovoPsd.AddShapeLayer();

    var nuovoShape = GenerateNewShape(nuovoPsd.Size);
    List<IPathShape> nuoveForme = new List<IPathShape>();
    nuoveForme.Add(nuovoShape);
    layer.Path.SetItems(nuoveForme.ToArray());

    layer.Update();

    nuovoPsd.Save(outputFile);
}

using (PsdImage immagine = (PsdImage)Image.Load(outputFile))
{
    AssertAreEqual(2, immagine.Layers.Length);

    ShapeLayer shapeLayer = immagine.Layers[1] as ShapeLayer;
    ColorFillSettings riempimentoInterno = shapeLayer.Fill as ColorFillSettings;
    IStrokeSettings impostazioniTratto = shapeLayer.Stroke;
    ColorFillSettings riempimentoTratto = shapeLayer.Stroke.Fill as ColorFillSettings;

    AssertAreEqual(1, shapeLayer.Path.GetItems().Length); // 1 Forma
    AssertAreEqual(3, shapeLayer.Path.GetItems()[0].GetItems().Length); // 3 nodi in una forma

    AssertAreEqual(-16127182, riempimentoInterno.Color.ToArgb()); // ff09eb32

    AssertAreEqual(7.41, impostazioniTratto.Size);
    AssertAreEqual(false, impostazioniTratto.Enabled);
    AssertAreEqual(StrokePosition.Center, impostazioniTratto.LineAlignment);
    AssertAreEqual(LineCapType.ButtCap, impostazioniTratto.LineCap);
    AssertAreEqual(LineJoinType.MiterJoin, impostazioniTratto.LineJoin);
    AssertAreEqual(-16777216, riempimentoTratto.Color.ToArgb()); // ff000000
}

PathShape GenerateNewShape(Size dimensioniImmagine)
{
    var nuovaForma = new PathShape();

    PointF punto1 = new PointF(20, 100);
    PointF punto2 = new PointF(200, 100);
    PointF punto3 = new PointF(300, 10);

    BezierKnotRecord[] nodiBezier = new BezierKnotRecord[]
    {
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(punto1, dimensioniImmagine),
                          PointFToResourcePoint(punto1, dimensioniImmagine),
                          PointFToResourcePoint(punto1, dimensioniImmagine),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(punto2, dimensioniImmagine),
                          PointFToResourcePoint(punto2, dimensioniImmagine),
                          PointFToResourcePoint(punto2, dimensioniImmagine),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(punto3, dimensioniImmagine),
                          PointFToResourcePoint(punto3, dimensioniImmagine),
                          PointFToResourcePoint(punto3, dimensioniImmagine),
                      }
         },
    };

    nuovaForma.SetItems(nodiBezier);

    return nuovaForma;
}

Point PointFToResourcePoint(PointF punto, Size dimensioniImmagine)
{
    return new Point(
        (int)Math.Round(punto.Y * (ImgToPsdRatio / dimensioniImmagine.Height)),
        (int)Math.Round(punto.X * (ImgToPsdRatio / dimensioniImmagine.Width)));
}

void AssertAreEqual(object atteso, object effettivo, string messaggio = null)
{
    if (!object.Equals(atteso, effettivo))
    {
        throw new Exception(messaggio ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1966. Specifico file PSD non può essere esportato utilizzando Aspose.PSD**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "1966source.psd");
string outputPng = Path.Combine(cartellaOutput, "output.png");

using (var immaginePsd = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    immaginePsd.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
