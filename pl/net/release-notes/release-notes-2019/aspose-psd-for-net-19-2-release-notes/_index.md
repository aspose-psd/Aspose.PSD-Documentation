---
title: Aspose.PSD dla .NET 19.2 - Notatki o wydaniu
type: docs
weight: 110
url: /pl/net/aspose-psd-dla-net-19-2-notatki-o-wydaniu/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki o wydaniu dla Aspose.PSD dla .NET 19.2

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-97|Dodanie obsługi warstw wypełnienia: Wypełnienie kolorem|Funkcja|
|PSDNET-98|Dodanie obsługi warstw wypełnienia: Wypełnienie gradientem|Funkcja|
|PSDNET-105|Wsparcie dla GdFlResource|Funkcja|
|PSDNET-106|Wsparcie dla VmskResource|Funkcja|
|PSDNET-109|Przeniesienie rzeczywistych źródeł Aspose.Imaging do Aspose.PSD|Udoskonalenie|
|PSDNET-92|Dodanie obsługi częściowego ładowania dla niektórych metod|Udoskonalenie|
|PSDNET-110|Wydajność PSD spadła kilkakrotnie|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillType
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientName
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Gradient
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Pattern
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IColorFillSettings.Color
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.TransparencyPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.MedianPointLocation
- M:Aspose.PSD.Extensions.RectangleExtensions.UnionWith(Aspose.PSD.RectangleF,Aspose.PSD.RectangleF)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.Points
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.ProducePathRecord(System.Byte[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.PathFillRuleRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClipboardRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.InitialFillRuleRecord
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.Signature
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientInterval
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.AlignWithLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.TransparencyPoints
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AddColorPoint
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AddTransparencyPoint
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Linear
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Radial
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Angle
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Reflected
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Diamond
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.ShapeBurst
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GenerateLfx2ResourceNodes
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Color
## **Przykłady użycia:**
**PSDNET-97. Dodanie obsługi warstw wypełnienia: Wypełnienie kolorem**

{{< highlight java >}}

 // Dodanie obsługi warstw wypełnienia: Wypełnienie kolorem

string nazwaPlikuZrodlowego = "WarstwaWypelnieniaKolorem.psd";

string sciezkaEksportu = "WarstwaWypelnieniaKolorem_wyjscie.psd";

string sciezkaEksportuPng = "WarstwaWypelnieniaKolorem_wyjscie.png";

var obraz = (PsdImage) Image.Load(nazwaPlikuZrodlowego);

using(obraz) {

 foreach(var warstwa in obraz.Layers) {

  if (warstwa is FillLayer) {

   var warstwaWypelnienia = (FillLayer) warstwa;

   if (warstwaWypelnienia.FillSettings.FillType != FillType.Color) {

    throw new Exception("Niepoprawna warstwa wypełnienia");

   }

   var ustawienia = (IColorFillSettings) warstwaWypelnienia.FillSettings;

   ustawienia.Color = Color.Red;

   warstwaWypelnienia.Update(); 

   obraz.Save(sciezkaEksportu);   

   break;

  }

 }

}

{{< /highlight >}}

**PSDNET-98. Dodanie obsługi warstw wypełnienia: Wypełnienie gradientem**

{{< highlight java >}}

 // Obsługa warstwy wypełnienia gradientem

string nazwaPlikuZrodlowego = "ZlozonaWarstwaWypelnieniaGradientem.psd";

string plikWyjsciowy = "ZlozonaWarstwaWypelnieniaGradientem_wyjscie.psd";

var obraz = (PsdImage) Image.Load(nazwaPlikuZrodlowego);

using(obraz) {

 foreach(var warstwa in obraz.Layers) {

  if (warstwa is FillLayer) {

   var warstwaWypelnienia = (FillLayer) warstwa;

   if (warstwaWypelnienia.FillSettings.FillType != FillType.Gradient) {

    throw new Exception("Niepoprawna warstwa wypełnienia");

   }

   var ustawienia = (IGradientFillSettings) warstwaWypelnienia.FillSettings;

   if (Math.Abs(ustawienia.Angle - 45) > 0.25 ||

    ustawienia.Dither != true ||

    ustawienia.AlignWithLayer != false ||

    ustawienia.Reverse != false ||

    Math.Abs(ustawienia.HorizontalOffset - (-39)) > 0.25 ||

    Math.Abs(ustawienia.VerticalOffset - (-5)) > 0.25 ||

    ustawienia.TransparencyPoints.Length != 3 ||

    ustawienia.ColorPoints.Length != 2 ||

    Math.Abs(100.0 - ustawienia.TransparencyPoints[0].Opacity) > 0.25 ||

    ustawienia.TransparencyPoints[0].Location != 0 ||

    ustawienia.TransparencyPoints[0].MedianPointLocation != 50 ||

    ustawienia.ColorPoints[0].Color != Color.FromArgb(203, 64, 140) ||

    ustawienia.ColorPoints[0].Location != 0 ||

    ustawienia.ColorPoints[0].MedianPointLocation != 50) {

    throw new Exception("Niepoprawne odczytanie wypełnienia gradientem");

   }

   ustawienia.Angle = 0.0;

   ustawienia.Dither = false;

   ustawienia.AlignWithLayer = true;

   ustawienia.Reverse = true;

   ustawienia.HorizontalOffset = 25;

   ustawienia.VerticalOffset = -15;

   var punktyKoloru = new List < IGradientColorPoint > (ustawienia.ColorPoints);

   var punktyPrzezroczystosci = new List < IGradientTransparencyPoint > (ustawienia.TransparencyPoints);

   punktyKoloru.Add(new GradientColorPoint() {

    Color = Color.Violet,

     Location = 4096,

     MedianPointLocation = 75

   });

   punktyKoloru[1].Location = 3000;

   punktyPrzezroczystosci.Add(new GradientTransparencyPoint() {

    Opacity = 80.0,

     Location = 4096,

     MedianPointLocation = 25

   });

   punktyPrzezroczystosci[2].Location = 3000;

   ustawienia.ColorPoints = punktyKoloru.ToArray();

   ustawienia.TransparencyPoints = punktyPrzezroczystosci.ToArray();

   warstwaWypelnienia.Update();

   obraz.Save(plikWyjsciowy, new PsdOptions(obraz));

   break;

  }

 }

}

{{< /highlight >}}

**PSDNET-105. Wsparcie dla GdFlResource**

{{< highlight java >}}

 // Wsparcie dla GdFlResource

string nazwaPlikuZrodlowego = "ZlozonaWarstwaWypelnieniaGradientem.psd";

string sciezkaEksportu = "ZlozonaWarstwaWypelnieniaGradientem_po.psd";

var obraz = (PsdImage) Image.Load(nazwaPlikuZrodlowego);

using(obraz) {

 foreach(var warstwa in obraz.Layers) {

  if (warstwa is FillLayer) {

   var warstwaWypelnienia = (FillLayer) warstwa;

   var zasoby = warstwaWypelnienia.Resources;

   foreach(var zasob in zasoby) {

    if (zasob is GdFlResource) {

     // Odczyt

     var zasobGdFl = (GdFlResource) zasob;

     if (zasobGdFl.AlignWithLayer != false ||

      (Math.Abs(zasobGdFl.Angle - 45.0) > 0.001) ||

      zasobGdFl.Dither != true ||

      zasobGdFl.Reverse != false ||

      zasobGdFl.Color != Color.Empty ||

      Math.Abs(zasobGdFl.HorizontalOffset - (-39)) > 0.001 ||

      Math.Abs(zasobGdFl.VerticalOffset - (-5)) > 0.001 ||

      zasobGdFl.TransparencyPoints.Length != 3 ||

      zasobGdFl.ColorPoints.Length != 2) {

      throw new Exception("Parametry zasobu zostały źle odczytane");

     }

     var punktyPrzezroczystosci = zasobGdFl.TransparencyPoints;

     if (Math.Abs(100.0 - punktyPrzezroczystosci[0].Opacity) > 0.25 ||

      punktyPrzezroczystosci[0].Location != 0 ||

      punktyPrzezroczystosci[0].MedianPointLocation != 50 ||

      Math.Abs(50.0 - punktyPrzezroczystosci[1].Opacity) > 0.25 ||

      punktyPrzezroczystosci[1].Location != 2048 ||

      punktyPrzezroczystosci[1].MedianPointLocation != 50 ||

      Math.Abs(100.0 - punktyPrzezroczystosci[2].Opacity) > 0.25 ||

      punktyPrzezroczystosci[2].Location != 4096 ||

      punktyPrzezroczystosci[2].MedianPointLocation != 50) {

      throw new Exception("Punkty przezroczystości gradientu zostały źle odczytane");

     }

     var punktyKoloru = zasobGdFl.ColorPoints;

     if (punktyKoloru[0].Color != Color.FromArgb(203, 64, 140) ||

      punktyKoloru[0].Location != 0 ||

      punktyKoloru[0].MedianPointLocation != 50 ||

      punktyKoloru[1].Color != Color.FromArgb(203, 0, 0) ||

      punktyKoloru[1].Location != 4096 ||

      punktyKoloru[1].MedianPointLocation != 50) {

      throw new Exception("Punkty koloru gradientu zostały źle odczytane");

     }

     // Edycja

     zasobGdFl.Angle = 30.0;

     zasobGdFl.Dither = false;

     zasobGdFl.AlignWithLayer = true;

     zasobGdFl.Reverse = true;

     zasobGdFl.HorizontalOffset = 25;

     zasobGdFl.VerticalOffset = -15;

     var nowePunktyKoloru = new List < IGradientColorPoint > (zasobGdFl.ColorPoints);

     var nowePunktyPrzezroczystosci = new List < IGradientTransparencyPoint > (zasobGdFl.TransparencyPoints);

     nowePunktyKoloru.Add(new GradientColorPoint() {

      Color = Color.Violet,

       Location = 4096,

       MedianPointLocation = 75

     });

     punktyKoloru[1].Location = 3000;

     nowePunktyPrzezroczystosci.Add(new GradientTransparencyPoint() {

      Opacity = 80.0,

       Location = 4096,

       MedianPointLocation = 25

     });

     punktyPrzezroczystosci[2].Location = 3000;

     zasobGdFl.ColorPoints = nowePunktyKoloru.ToArray();

     zasobGdFl.TransparencyPoints = nowePunktyPrzezroczystosci.ToArray();

     obraz.Save(sciezkaEksportu);

    }

    break;

   }

   break;

  }

 }

}   

{{< /highlight >}}

**PSDNET-106. Wsparcie dla VmskResource**

{{< highlight java >}}  

 // Wsparcie dla VmskResource

static void PrzykladWsparciaDlaVmskResource() {

 string nazwaPlikuZrodlowego = "Prostokat.psd";

 string sciezkaEksportu = "Prostokat_zmieniony.psd";

 var obraz = (PsdImage) Image.Load(nazwaPlikuZrodlowego);

 using(obraz) {

  var zasob = PobierzZasobVmsk(obraz);

  // Odczyt

  if (zasob.IsDisabled != false ||

   zasob.IsInverted != false ||

   zasob.IsNotLinked != false ||

   zasob.Paths.Length != 7 ||

   zasob.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

   zasob.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

   zasob.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

   zasob.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

   zasob.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

   zasob.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

   zasob.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked) {

   throw new Exception("Zasób VmskResource został źle odczytany");

  }

  var regulaWypelnieniaSciezka = (PathFillRuleRecord) zasob.Paths[0];

  var regulaWypelnieniaPoczatkowa = (InitialFillRuleRecord) zasob.Paths[1];

  var dlugoscSciezki = (LengthRecord) zasob.Paths[2];

  // Reguła wypełnienia ścieżki nie zawiera dodatkowych informacji

  if (regulaWypelnieniaSciezka.Type != VectorPathType.PathFillRuleRecord ||

   regulaWypelnieniaPoczatkowa.Type != VectorPathType.InitialFillRuleRecord ||

   regulaWypelnieniaPoczatkowa.IsFillStartsWithAllPixels != false ||

   dlugoscSciezki.Type != VectorPathType.ClosedSubpathLengthRecord ||

   dlugoscSciezki.IsClosed != true ||

   dlugoscSciezki.IsOpen != false) {

   throw new Exception("Ścieżki zasobu zostały źle odczytane");

  }

  // Edycja

  zasob.IsDisabled = true;

  zasob.IsInverted = true;

  zasob.IsNotLinked = true;

  var wezelBeziera = (BezierKnotRecord) zasob.Paths[3];

  wezelBeziera.Points[0] = new Point(0, 0);

  wezelBeziera = (BezierKnotRecord) zasob.Paths[4];

  wezelBeziera.Points[0] = new Point(8039797, 10905190);

  regulaWypelnieniaPoczatkowa.IsFillStartsWithAllPixels = true;

  dlugoscSciezki.IsClosed = false;

  obraz.Save(sciezkaEksportu);

 }

}

static VmskResource PobierzZasobVmsk(PsdImage obraz) {

 var warstwa = obraz.Layers[1];

 VmskResource zasob = null;

 var zasoby = warstwa.Resources;

 for (int i = 0; i < zasoby.Length; i++) {

  if (zasoby[i] is VmskResource) {

   zasob = (VmskResource) zasoby[i];

   break;

  }

 }

 if (zasob == null) {

  throw new Exception("Zasób VmskResource nie został znaleziony");

 }

 return zasob;

} 

{{< /highlight >}}

**PSDNET-110. Wydajność PSD spadła kilkakrotnie**

{{< highlight java >}}

  // Wydajność PSD spadła kilkakrotnie

string nazwaPlikuZrodlowego = "1.psd";

string nazwaPlikuPng = "imaging3203.png";

string nazwaPlikuPsd = "imaging3203.psd";

var stoper = new Stopwatch();

using(PsdImage obraz = Image.Load(nazwaPlikuZrodlowego) as PsdImage) {

 stoper.Start();

 obraz.Save(nazwaPlikuPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 obraz.Save(nazwaPlikuPsd, new PsdOptions());

 stoper.Stop();

}

Console.WriteLine("MINĘŁO: ", stoper.Elapsed);

{{< /highlight >}}