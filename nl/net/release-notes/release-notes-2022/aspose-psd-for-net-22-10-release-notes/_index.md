---
title: Aspose.PSD voor .NET 22.10 - Release-opmerkingen
type: docs
weight: 30
url: /nl/net/aspose-psd-voor-net-22-10-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Deze release heeft een regressie in het geval van 16-bits exports, dus we raden voorzichtigheid aan bij het gebruik van deze functie in deze release.
Bij gebruik van 16-bits beeldverwerking als belangrijkste functionaliteit, raden wij af om Aspose.PSD bij te werken naar 22.9-22.10.

We werken aan oplossingen voor deze problemen.

{{% /alert %}}

|**Belangrijkheid**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-1287|Verwijder verouderde eigenschappen in Lfx2Resource|Verbetering|
|PSDNET-1071|Aspose.PSD kan PSD-bestand (RGB/16-bits) met ZipWithoutPrediction-compressie niet openen|Bug|
|PSDNET-1257|Tijdlijn effecten verdwijnen en worden vreemd weergegeven (in Photoshop)|Bug|
|PSDNET-1278|Transparantie werkt niet voor het Slageffect met Binnen Positie|Bug|
|PSDNET-1279|Regressie: Fout bij het openen van een PSD-bestand|Bug|
|PSDNET-1284|De tekstupdate mislukt met enkele Aziatische symbolen. Fout bij het verwerken van een specifiek symbool|Bug|
|PSDNET-1291|De tekstupdate mislukt met enkele Aziatische symbolen. Fout bij het renderen van een specifiek symbool|Bug|
|PSDNET-1292|Fout bij het openen van het geëxporteerde bestand door Photoshop na het opslaan van specifieke Aziatische symbolen|Bug|


## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- Geen


# **Verwijderde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Gebruik voorbeelden:**

**PSDNET-1071. Aspose.PSD kan PSD-bestand (RGB/16-bits) met ZipWithoutPrediction-compressie niet openen**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "uit_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Tijdlijn effecten verdwijnen en worden vreemd weergegeven (in Photoshop)**

{{< highlight csharp >}}
string bronbestand = "clearFile.psd";
string uitvoerbestand = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(bronbestand))
{
    // Maak tijdlijn met een paar frames.
    Tijdlijn tijdlijn = Tijdlijn.InitialiserenVan(psdImage);
    var laagIds = tijdlijn.LaagIds;

    Lijst<Kader> frames = nieuwe Lijst<Kader>(tijdlijn.Frames);
    voor (int i = 0; i < 3; i++)
    {
        frames.Add(new Kader(tijdlijn));
    }
    tijdlijn.Frames = frames.ToArray();

    tijdlijn.Frames[1].LaagStates[laagIds[1]].StaatEffecten.ToevoegenKleurOverlay();

    tijdlijn.Frames[2].LaagStates[laagIds[1]].StaatEffecten.ToevoegenGradientOverlay();
    tijdlijn.Frames[2].LaagStates[laagIds[1]].StaatEffecten.IsZichtbaar = false;

    tijdlijn.ToepassenOp(psdImage);

    psdImage.Save(uitvoerbestand);
}
{{< /highlight >}}

**PSDNET-1278. Transparantie werkt niet voor het Slageffect met Binnen Positie**

{{< highlight csharp >}}
string bronbestand = "psdnet1278.psd";
string uitvoer = "uit_1278.png";

using (var image = (PsdImage)Image.Load(bronbestand, new PsdLaadOpties() { LaadEffectenResource = true }))
{
    image.Save(uitvoer, new PngOpties());
}
{{< /highlight >}}

**PSDNET-1279. Regressie: Fout bij het openen van een PSD-bestand**

{{< highlight csharp >}}
string bronbestand = "AllTypesLayerPsd.psd";
string uitvoerPsd = "uit_1279.psd";

using (var image = (PsdImage) Afbeelding.Laden(bronbestand))
{
    image.Save(uitvoerPsd);
}
{{< /highlight >}}

**PSDNET-1284. De tekstupdate mislukt met enkele Aziatische symbolen. Fout bij het verwerken van een specifiek symbool**

{{< highlight csharp >}}
string testGegevens = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testGegevens = testGegevens.Substring(25, 1); // selecteer het problematische symbool

string srcBestand = "TestBestandVoorAziatischeTekensGroot.psd";
string uitvoer = "output.psd";

using (var image = (PsdImage)Afbeelding.Laden(srcBestand))
{
    var laag = (TekstLaag)image.Lagen[0];
    laag.UpdateTekst(testGegevens);
    image.Save(uitvoer);
}
{{< /highlight >}}

**PSDNET-1287. Verwijder verouderde eigenschappen in Lfx2Resource**

{{< highlight csharp >}}
string src = "bestandMetEffecten.psd";
string uitvoer = "output.psd";

using (var psdImage = (PsdImage)Afbeelding.Laden(src, new PsdLaadOpties() { LaadEffectenResource = true }))
{
    var laag = psdImage.Lagen[1];
    var effect = laag.MengOpties.Effecten[0];

    // Update effect BlendMode optie
    effect.BlendMode = BlendModus.Verduisteren;

    // Update effect Dekking optie
    effect.Dekking = 128; // 50%

    // Update vulkleur optie van slag effect
    var slagInstellingen = (IColorFillSettings)((SlagEffect)effect).VulInstellingen;
    slagInstellingen.Kleur = Kleur.Donkerrood;

    psdImage.Save(uitvoer);
}
{{< /highlight >}}

**PSDNET-1291. De tekstupdate mislukt met enkele Aziatische symbolen. Fout bij het renderen van een specifiek symbool**

{{< highlight csharp >}}
string testGegevens = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿 
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testGegevens = testGegevens.Substring(40, 25); // selecteer de problematische symbolen

string srcBestand = "TestBestandVoorAziatischeTekensGroot 2.psd";
string uitvoer = "output.psd";

using (var image = (PsdImage)Afbeelding.Laden(srcBestand))
{
    var laag = (TekstLaag)image.Lagen[0];
    laag.UpdateTekst(testGegevens);
    image.Save(uitvoer);
}
{{< /highlight >}}

**PSDNET-1292. Fout bij het openen van het geëxporteerde bestand door Photoshop na het opslaan van specifieke Aziatische symbolen**

{{< highlight csharp >}}
string testGegevens = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcBestand = "TestBestandVoorAziatischeTekensGroot 2.psd";
string uitBestand = "output.psd";

using (var image = (PsdImage)Afbeelding.Laden(srcBestand))
{
    var laag = (TekstLaag)image.Lagen[0];
    laag.UpdateTekst(testGegevens);

    image.Save(uitBestand);
}
{{< /highlight >}}
