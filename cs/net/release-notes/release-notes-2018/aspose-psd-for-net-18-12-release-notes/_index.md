---
title: Aspose.PSD pro .NET 18.12 - Poznámky k vydání
type: docs
weight: 10
url: /cs/net/aspose-psd-for-net-18-12-release-notes/
---

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-76|Podpora vrstvy obrysu|Funkce|
|PSDNET-83|Podpora efektu přechodu|Funkce|
|PSDNET-84|Podpora efektu vzoru|Funkce|
|PSDNET-89|Přidání možnosti přidat nově vytvořenou běžnou vrstvu do obraze Psd|Funkce|
|PSDNET-93|Po aktualizaci obsahu textové vrstvy s "\\" (zpětné lomítko) znakem není možné otevřít výsledný soubor v aplikaci Photoshop|Chyba|
|PSDNET-39|Po exportu s překročenými daty obrazu v režimu barev CMYK jsou obrázky rozbité|Chyba|
|PSDNET-52|Možné: Rotace v PSD nefunguje|Chyba|
|PSDNET-88|Možné: Metody oříznutí v Aspose.Psd nefungují|Chyba|
|PSDNET-91|Použití změn Aspose.Imaging v Aspose.PSD|Vylepšení|

## **Změny ve veřejném API**
Metoda    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Třída    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Metoda    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Metoda    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Pole/Výčet    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Metoda    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Třída    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Vlastnost    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Příklady použití:**
**PSDNET-76. Podpora vrstvy obrysu**

**1) Typ výplně - Vzor**

{{< highlight java >}}

     // Efekt obrysu. Typ výplně - Vzor. Příklad

    string zdrojovýSoubor = "Obrys.psd";

    string cestaExportu = "ObrysZmenaVzoru.psd";

    var možnostiNačtení = new MožnostiNačteníPsd()

    {

        NačístZdrojeEfektů = true

    };

    // Příprava nových dat

    var novýVzor = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

    };

   var novéHraniceVzoru = new Rectangle(0, 0, 4, 4);

   var id = Guid.NewGuid();

    using (var im = (ObrázekPsd)Image.Load(zdrojovýSoubor, možnostiNačtení))

    {

         var obrysVzoru = (EfektObrysu)im.Vrstvy[3].MožnostiSmíchávání.Efekty[0];

         Assert.AreEqual(BlendMode.Normal, obrysVzoru.RežimSmíchávání);

         Assert.AreEqual(255, obrysVzoru.Průhlednost);

         Assert.AreEqual(true, obrysVzoru.JeViditelný);

         var nastaveníVýplně = (NastaveníVýplněVzorem)obrysVzoru.NastaveníVýplně;

         Assert.AreEqual(FillType.Pattern, nastaveníVýplně.TypVýplně);

         obrysVzoru.Průhlednost = 127;

         obrysVzoru.RežimSmíchávání = BlendMode.Color;

         PattResource zdroj;

         foreach (var globálníZdrojVrstvy in im.GlobálníZdrojeVrstev)

         {

             if (globálníZdrojVrstvy is PattResource)

             {

                  zdroj = (PattResource)globálníZdrojVrstvy;

                  zdroj.IdVzoru = id.ToString();

                  zdroj.Název = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";        

                  zdroj.NastavVzor(novýVzor, novéHraniceVzoru);               

             }

         }

         ((NastaveníVýplněVzorem)nastaveníVýplně).NázevVzoru = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";

         ((NastaveníVýplněVzorem)nastaveníVýplně).IdVzoru = id.ToString() + "\0";

        im.Save(cestaExportu);

    }

    // Tester souboru po editaci

    using (var im = (ObrázekPsd)Image.Load(zdrojovýSoubor, možnostiNačtení))

    {

        var obrysVzoru = (EfektObrysu)im.Vrstvy[3].MožnostiSmíchávání.Efekty[0];

        PattResource zdroj = null;

        foreach (var globálníZdrojVrstvy in im.GlobálníZdrojeVrstev)

        {

            if (globálníZdrojVrstvy is PattResource)

            {

                zdroj = (PattResource)globálníZdrojVrstvy;

            }

        }

        if (zdroj == null)

        {

            throw new Exception("Nenalezen zdroj vzoru");

        }

        // Kontrola dat vzoru

        Assert.AreEqual(novýVzor, zdroj.PatternData);

        Assert.AreEqual(novéHraniceVzoru, new Rectangle(0, 0, zdroj.Width, zdroj.Height));

        Assert.AreEqual(id.ToString(), zdroj.IdVzoru);

        Assert.AreEqual(BlendMode.Color, obrysVzoru.RežimSmíchávání);

        Assert.AreEqual(127, obrysVzoru.Průhlednost);

        var nastaveníVýplně = (NastaveníVýplněVzorem)nastaveníVýplně;

        Assert.AreEqual(FillType.Pattern, nastaveníVýplně.TypVýplně);

    }

{{< /highlight >}}

**2) Typ výplně - Přechod**

{{< highlight java >}}

     // Efekt obrysu. Typ výplně - Přechod. Příklad

    string zdrojovýSoubor = "Obrys.psd";

    string cestaExportu = "ObrysPřechodZměněn.psd";

    var možnostiNačtení = new MožnostiNačteníPsd()

    {

        NačístZdrojeEfektů = true

    };

    using (var im = (ObrázekPsd)Image.Load(zdrojovýSoubor, možnostiNačtení))

    {

        var obrysPřechodu = (EfektObrysu)im.Vrstvy[2].MožnostiSmíchávání.Efekty[0];

        Assert.AreEqual(BlendMode.Normal, obrysPřechodu.RežimSmíchávání);

        Assert.AreEqual(255, obrysPřechodu.Průhlednost);

        Assert.AreEqual(true, obrysPřechodu.JeViditelný);

        var nastaveníVýplně = (NastaveníPřechoduVýplně)obrysPřechodu.NastaveníVýplně;

        Assert.AreEqual(Color.Black, nastaveníVýplně.Barva);

        Assert.AreEqual(FillType.Gradient, nastaveníVýplně.TypVýplně);

        Assert.AreEqual(true, nastaveníVýplně.ZarovnatSvrstvou);

        Assert.AreEqual(GradientType.Linear, nastaveníVýplně.TypPřechodu);

        Assert.IsTrue(Math.Abs(90 - nastaveníVýplně.Uhel) < 0.001, "Úhel je nesprávný");

        Assert.AreEqual(false, nastaveníVýplně.Dither);

        Assert.IsTrue(Math.Abs(0 - nastaveníVýplně.HorizontálníPosun) < 0.001, "Horizontální posun je nesprávný");

        Assert.IsTrue(Math.Abs(0 - nastaveníVýplně.VertikálníPosun) < 0.001, "Vertikální posun je nesprávný");

        Assert.AreEqual(false, nastaveníVýplně.Převrátit);

        // Barvy bodů

        var barevnéBody = nastaveníVýplně.BarevnéBody;

        Assert.AreEqual(2, barevnéBody.Délka);

        Assert.AreEqual(Color.Black, barevnéBody[0].Barva);

        Assert.AreEqual(0, barevnéBody[0].Umístění);

        Assert.AreEqual(50, barevnéBody[0].UmístěníProstředníhoBodu);

        Assert.AreEqual(Color.White, barevnéBody[1].Barva);

        Assert.AreEqual(4096, barevnéBody[1].Umístění);

        Assert.AreEqual(50, barevnéBody[1].UmístěníProstředníhoBodu);

        // Body průhlednosti

        var bodyPrůhlednosti = nastaveníVýplně.BodyPrůhlednosti;

        Assert.AreEqual(2, bodyPrůhlednosti.Délka);

        Assert.AreEqual(0, bodyPrůhlednosti[0].Umístění);

        Assert.AreEqual(50, bodyPrůhlednosti[0].UmístěníProstředníhoBodu);

        Assert.AreEqual(100, bodyPrůhlednosti[0].Průhlednost);

        Assert.AreEqual(4096, bodyPrůhlednosti[1].Umístění);

        Assert.AreEqual(50, bodyPrůhlednosti[1].UmístěníProstředníhoBodu);

        Assert.AreEqual(100, bodyPrůhlednosti[1].Průhlednost);

        // Testování úprav

        nastaveníVýplně.Barva = Color.Green;

        obrysPřechodu.Průhlednost = 127;

        obrysPřechodu.RežimSmíchávání = BlendMode.Color;

        nastaveníVýplně.ZarovnatSvrstvou = false;

        nastaveníVýplně.TypPřechodu = GradientType.Radial;

        nastaveníVýplně.Uhel = 45;

        nastaveníVýplně.Dither = true;

        nastaveníVýplně.HorizontálníPosun = 15;

        nastaveníVýplně.VertikálníPosun = 11;

        nastaveníVýplně.Převrátit = true;

        // Přidání nového barevného bodu

        var barevnýBod = nastaveníVýplně.PřidatBarevnýBod();

        barevnýBod.Barva = Color.Green;        

        barevnýBod.Umístění = 4096;

        barevnýBod.UmístěníProstředníhoBodu = 75;

        // Změna umístění předchozího bodu

        nastaveníVýplně.BarevnéBody[1].Umístění = 1899;

        // Přidání nového bodu průhlednosti

        var bodPrůhlednosti = nastaveníVýplně.PřidatBodPrůhlednosti();

        bodPrůhlednosti.Průhlednost = 25;

        bodPrůhlednosti.UmístěníProstředníhoBodu = 25;

        bodPrůhlednosti.Umístění = 4096;

        // Změna umístění předchozího bodu průhlednosti

        nastaveníVýplně.BodyPrůhlednosti[1].Umístění = 2411;

        im.Save(cestaExportu);

    }

    // Tester souboru po editaci

    using (var im = (ObrázekPsd)Image.Load(zdrojovýSoubor, možnostiNačtení))

    {

         var obrysPřechodu = (EfektObrysu)im.Vrstvy[2].MožnostiSmíchávání.Efekty[0];

         Assert.AreEqual(BlendMode.Color, obrysPřechodu.RežimSmíchávání);

         Assert.AreEqual(127, obrysPřechodu.Průhlednost);

         Assert.AreEqual(true, obrysPřechodu.JeViditelný);

         var nastaveníVýplně = (NastaveníPřechoduVýplně)obrysPřechodu.NastaveníVýplně;

         Assert.AreEqual(Color.Green, nastaveníVýplně.Barva);

         Assert.AreEqual(FillType.Gradient, nastaveníVýplně.TypVýplně);

         // Kontrola barevných bodů

         Assert.AreEqual(3, nastaveníVýplně.BarevnéBody.Délka);

         var bod = nastaveníVýplně.BarevnéBody[0];

         Assert.AreEqual(50, bod.UmístěníProstředníhoBodu);

         Assert.AreEqual(Color.Black, bod.Barva);

         Assert.AreEqual(0, bod.Umístění);

         bod = nastaveníVýplně.BarevnéBody[1];

         Assert.AreEqual(50, bod.UmístěníProstředníhoBodu);

         Assert.AreEqual(Color.White, bod.Barva);

         Assert.AreEqual(1899, bod.Umístění);

         bod = nastaveníVýplně.BarevnéBody[2];

         Assert.AreEqual(75, bod.UmístěníProstředníhoBodu);

         Assert.AreEqual(Color.Green, bod.Barva);

         Assert.AreEqual(4096, bod.Umístění);

         // Kontrola bodů průhlednosti

         Assert.AreEqual(3, nastaveníVýplně.BodyPrůhlednosti.Délka);

         var bodPrůhlednosti = nastaveníVýplně.BodyPrůhlednosti[0];

         Assert.AreEqual(50, bodPrůhlednosti.UmístěníProstředníhoBodu);

         Assert.AreEqual(100, bodPrůhlednosti.Průhlednost);

         Assert.AreEqual(0, bodPrůhlednosti.Umístění);

         bodPrůhlednosti = nastaveníVýplně.BodyPrůhlednosti[1];

         Assert.AreEqual(50, bodPrůhlednosti.UmístěníProstředníhoBodu);

         Assert.AreEqual(100, bodPrůhlednosti.Průhlednost);

         Assert.AreEqual(2411, bodPrůhlednosti.Umístění);

         bodPrůhlednosti = nastaveníVýplně.BodyPrůhlednosti[2];

         Assert.AreEqual(25, bodPrůhlednosti.UmístěníProstředníhoBodu);

         Assert.AreEqual(25, bodPrůhlednosti.Průhlednost);

         Assert.AreEqual(4096, bodPrůhlednosti.Umístění);

    }

{{< /highlight >}}

**PSDNET-84. Podpora efektu vzoru.**

{{< highlight java >}}

    // Efekt překrytí vzorem. Příklad

    string zdrojovýSoubor = "PřekrytíVzorem.psd";

    string cestaExportu = "PřekrytíVzoruZměněno.psd";

    var novýVzor = new int[]

    {

        Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

        Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

    };

    var novéHraniceVzoru = new Rectangle(0, 0, 4, 2);

    var id = Guid.NewGuid();

    var novýNázevVzoru = "$$$/Presets/Patterns/Pattern=Nějaký nový název vzoru\0";

    var možnostiNačtení = new MožnostiNačteníPsd()

    {

        NačístZdrojeEfektů = true

    };

    using (var im = (ObrázekPsd)Image.Load(zdrojovýSoubor))

    {

        var staráVrstva = im.Vrstvy[0];

        var staréHranice = staráVrstva.Hranice;

        var staráVrstvaData = im.Vrstvy[0].NačístArgb32Pixely(staréHranice);

        var vrstvy = new Vrstva[4];

        for (int i = 0; i < 4; i++)

        {

            vrstvy[i] = im.PřidatBěžnouVrstvu();

            vrstvy[i].UložitArgb32Pixely(staréHranice, staráVrstvaData);

        }

        im.Resize(186, 602);

        vrstvy[0].Oříznout(new Rectangle(0, 0, 186, 159));

        vrstvy[1].Oříznout(new Rectangle(186, 0, 186, 159));

        vrstvy[2].Oříznout(new Rectangle(0, 159, 186, 142));

        vrstvy[3].Oříznout(new Rectangle(186, 159, 186, 142));

        staráVrstva.Zrušit();

        im.Vrstvy = vrstvy;

        var vrchníOkraj = 0;

        for (int i = 0; i < 4; i++)

        {

            var šířka = vrstvy[i].Šířka;

            var výška = vrstvy[i].Výška;

            vrstvy[i].Levý = 0;

            vrstvy[i].Horní = vrchníOkraj;

            vrstvy[i].Pravý = šířka;

            vrstvy[i].Dolní = výška + vrstvy[i].Horní;

            vrchníOkraj += vrstvy[i].Výška;

        }

        // Uložit psd

        im.Save(cestaExportu, new MožnostiPsd());

    }

{{< /highlight >}}

**PSDNET-93. Po aktualizaci obsahu textové vrstvy s "\\" (zpětná lomítka) znakem není možné otevřít výsledný soubor v aplikaci Photoshop.**

{{< highlight java >}}

 using (

var obrázek =

Image.Load(

"příklad.psd"))

{

if (!(obrázek is ObrázekPsd)) return;

                var psdObrázek = (ObrázekPsd)obrázek;

                var vrstvy = psdObrázek.Vrstvy;

                for (var index = vrstvy.Délka - 1; index >= 0; index--)

                {

                    var vrstva = vrstvy[index];

                    if (!(vrstva is TextováVrstva)) continue;

                    var textováVrstva = (TextováVrstva)vrstva;

                    textováVrstva.AktualizovatText("展 就");

                }

                var možnostiObrázku = new MožnostiPsd(psdObrázek);

                psdObrázek.Save("výsledek.psd", možnostiObrázku);

            }

{{< /highlight >}}

**PSDNET-39. Rozbité obrázky po exportu s překročenými daty obrazu v barevném režimu CMYK**

{{< highlight java >}}

     // Rozbité obrázky po exportu s překročenými daty obrazu v barevném režimu CMYK. Příklad

    string zdrojovýSoubor = "PřekročenýObrázekCmykSAdjustmentVrstvou.psd";

    string cestaExportu = "PřekročenýObrázekCmykSAdjustmentVrstvou.png";

    using (var im = (ObrázekPsd)Image.Load(zdrojovýSoubor))

    {        

        im.Save(cestaExportu, new MožnostiPng());

    }

{{< /highlight >}}

**~ PSDNET-52. Možné: Rotace v PSD nefunguje.**

{{< highlight java >}}

  // Rotace v PSD. Příklad

    string zdrojovýSoubor = "Klobouk.psd";

    var možnostiPng = new MožnostiPng() { TypBarevPng = PngColorType.TruecolorWithAlpha };

    // Celková rotace obrázku

    using (ObrázekPsd obrázek = (ObrázekPsd)Image.Load(zdrojovýSoubor))

    {

        for (int i = 0; i < 4; i++)

        {

            int úhel = i * 45;

            obrázek.Rotate(úhel);

            string názevSouboru = "KloboukOtočený" + úhel + ".png";

            obrázek.Save(názevSouboru, možnostiPng);

        }

    }

    // Rotace vrstvy

    using (ObrázekPsd obrázek = (ObrázekPsd)Image.Load(zdrojovýSoubor))

    {

        for (int i = 0; i < 4; i++)

        {

            int úhel = i * 45;

            obrázek.Vrstvy[1].Rotate(úhel);

            string názevSouboru = "VrstvaKloboukuOtočena" + úhel + ".png";

            obrázek.Save(názevSouboru, možnostiPng);

        }

    }       

{{< /highlight >}}