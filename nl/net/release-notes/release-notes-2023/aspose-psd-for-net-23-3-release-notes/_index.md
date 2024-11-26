---
title: Aspose.PSD voor .NET 23.3 - Release-opmerkingen
type: docs
weight: 100
url: /nl/net/aspose-psd-voor-net-23-3-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Trefwoord**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-146|Ondersteuning van Posterize Adjustment Layer|Functie|
|PSDNET-1366|Implementeer ondersteuning voor VscgResource|Functie|
|PSDNET-1437|Voeg ondersteuning toe voor PostResource resource voor gegevens van Posterize Adjustment Layer|Functie|
|PSDNET-931|Onjuiste export naar PNG-laag met Curves-aanpassing en CMYK-kleurmodus|Fout|
|PSDNET-1403|Stijl van paragraaf ontbreekt na het opslaan van het bestand en bijwerken van het bestand door PS|Fout|
|PSDNET-1453|Gebroken weergave van gloei- en schaduweffecten op tekst|Fout|


## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Vulkleurinstellingen.IPatroonVulkleurinstellingen.Hoek
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Vulkleurinstellingen.PatroonVulkleurinstellingen.Hoek
- T:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource
- M:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.#ctor
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.Handtekening
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.Sleutel
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.Lengte
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.PsdVersie
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.Items
- P:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.SleutelVoorGegevens
- M:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.Opslaan(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.Bestandsindelingen.Psd.Lagen.Laagbronnen.Slagbronnen.VscgResource.TypeToolSleutel


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-146. Ondersteuning van Posterize Adjustment Layer**

{{< highlight csharp >}}
string bronBestand = "zendeya_posterize.psd";
string uitvoerBestand = "zendeya_posterize_10.psd";

using (var afbeelding = (PsdImage)Image.Load(bronBestand, new PsdLoadOptions()))
{
    foreach (Laag laag in afbeelding.Lagen)
    {
        if (laag is PosterizeLayer)
        {
            ((PosterizeLayer)laag).Niveaus = 10;
            afbeelding.Save(uitvoerBestand);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Onjuiste export naar PNG-laag met Curves-aanpassing en CMYK-kleurmodus**

{{< highlight csharp >}}
string srcBestand = "input_LevelsLayerWithLayerMaskCmyk.psd";
string uitvoerBestand = "output_LevelsLayerWithLayerMaskCmykTest.png";
string uitvoerBestandPsd = "output.psd";

var psdLaadOpties = new PsdLoadOptions() { LaadEffectResouce = true };
using (PsdImage afbeelding = (PsdImage)Image.Load(srcBestand, psdLaadOpties))
{
    afbeelding.Save(uitvoerBestandPsd, new PsdOpties()); // de ', new PsdOptions()' veroorzaakt een fout.
    afbeelding.Save(uitvoerBestand, new PngOpties() { KleurType = PngKleurType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Implementeer ondersteuning voor VscgResource**

{{< highlight csharp >}}
string bronBestand = "StrokeInternalFill_src.psd";
string uitvoerBestand = "StrokeInternalFill_res.psd";

void ZijnGelijk(double verwacht, dubbel huidig, double tolerantie = 0.1)
{
    if (Math.Abs(verwacht - huidig) > tolerantie)
    {
        throw new Exception(
        $"Waarden zijn niet gelijk.\nVerwacht:{verwacht}\nResultaat:{huidig}\nVerschil:{verwacht - huidig}");
    }
}

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    VscgResource vscgResource = (VscgResource)afbeelding.Lagen[1].Bronnen[0];
    DescriptorStructure rgbKleurStructuur = (DescriptorStructure)vscgResource.Items[0];

    ZijnGelijk(89.8, ((DoubleStructure)rgbKleurStructuur.Structuren[0]).Waarde);
    ZijnGelijk(219.6, ((DoubleStructure)rgbKleurStructuur.Structuren[1]).Waarde);
    ZijnGelijk(34.2, ((DoubleStructure)rgbKleurStructuur.Structuren[2]).Waarde);

    ((DoubleStructure)rgbKleurStructuur.Structuren[0]).Waarde = 255d; // Rood
    ((DoubleStructure)rgbKleurStructuur.Structuren[1]).Waarde = 0d; // Groen
    ((DoubleStructure)rgbKleurStructuur.Structuren[2]).Waarde = 0d; // Blauw

    afbeelding.Save(uitvoerBestand);
}

// controleren van wijzigingen
using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestand))
{
    VscgResource vscgResource = (VscgResource)afbeelding.Lagen[1].Bronnen[0];
    DescriptorStructure rgbKleurStructuur = (DescriptorStructure)vscgResource.Items[0];

    ZijnGelijk(255, ((DoubleStructure)rgbKleurStructuur.Structuren[0]).Waarde);
    ZijnGelijk(0, ((DoubleStructure)rgbKleurStructuur.Structuren[1]).Waarde);
    ZijnGelijk(0, ((DoubleStructure)rgbKleurStructuur.Structuren[2]).Waarde);
}
{{< /highlight >}}

**PSDNET-1403. Stijl van paragraaf ontbreekt na het opslaan van het bestand en bijwerken van het bestand door PS**

{{< highlight csharp >}}
string bronBestand = "PSDTest3.psd";
string uitvoerBestand = "output.psd";

string[] nieuwTekst = new string[]
{
    "Titel \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage afbeelding = (PsdImage)Aspose.PSD.Image.Load(bronBestand))
{
    TextLayer laag2 = afbeelding.AddTextLayer("Nieuwe laag", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var tekstGegevensTL = laag2.TekstGegevens;

    ITextStyle standaardStijlTL = tekstGegevensTL.ProduceerDelen().Stijl;

    ITextParagraph standaardParagraafTL = tekstGegevensTL.ProduceerDelen().Paragraaf;
    ITextPortion[] nieuweDelenTL = tekstGegevensTL.ProduceerDelen(nieuwTekst, standaardStijlTL, standaardParagraafTL);

    nieuweDelenTL[0].Stijl.Lettergrootte = 14;
    nieuweDelenTL[0].Stijl.Lettertype = "TwCenMT-Bold";

    nieuweDelenTL[1].Stijl.Leidend = 20;
    nieuweDelenTL[1].Stijl.Lettergrootte = 10;
    nieuweDelenTL[1].Stijl.Lettertype = "TwCenMT-Bold";

    // Oude tekst verwijderen
    tekstGegevensTL.VerwijderDelen(0);

    // Nieuwe tekstdelen toevoegen
    foreach (var nieuwDeel in nieuweDelenTL)
    {
        tekstGegevensTL.VoegDeelToe(nieuwDeel);
    }

    tekstGegevensTL.WerkLaagGegevensBij();

    afbeelding.Save(uitvoerBestand);
}

using (PsdImage psdAfbeelding = (PsdImage)Aspose.PSD.Image.Load(uitvoerBestand))
{
    Txt2Resource txt2UitvoerResource = (Txt2Resource)psdAfbeelding.GlobaleLaagBronnen[1];
    byte[] bytes = txt2UitvoerResource.Gegevens;
    string txt2Gegevens = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Gegevens += (char)bytes[i];
    }

    string sleutel0 = @" >> /6 0 >> >> /1 "; // voorvoegsel voor lengte van paragraaf 0
    string sleutel1 = @" >> /6 1 >> >> /1 "; // voorvoegsel voor lengte van paragraaf 1
    int index0 = txt2Gegevens.IndexOf(sleutel0);
    int index1 = txt2Gegevens.IndexOf(sleutel1);

    string lengtePar0 = txt2Gegevens.Substring(index0 + sleutel0.Length, 1);
    string lengtePar1 = txt2Gegevens.Substring(index1 + sleutel1.Length, 3);

    string verwacht0 = nieuwTekst[0].Length.ToString();
    string verwacht1 = (nieuwTekst[1].Length + 1).ToString();

    if (lengtePar0 != verwacht0 || lengtePar1 != verwacht1)
    {
        throw new Exception(
            $"Lengte van paragrafen is onjuist.\nVerwacht: {verwacht0} en {verwacht1}\nResultaat: {lengtePar0} en {lengtePar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Voeg ondersteuning toe voor PostResource resource voor gegevens van Posterize Adjustment Layer**

{{< highlight csharp >}}
string bronBestand = "zendeya_posterize.psd";
string uitvoerBestand = "zendeya_posterize_10.psd";

using (var afbeelding = (PsdImage)Image.Load(bronBestand, new PsdLoadOptions()))
{
    Laag laag = afbeelding.Lagen[1];

    foreach (Laagbron bron in laag.Bronnen)
    {
        if (bron is PostResource)
        {
            ((PostResource)bron).Niveaus = 10;
            afbeelding.Save(uitvoerBestand);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Gebroken weergave van gloei- en schaduweffecten op tekst**

{{< highlight csharp >}}
string uitvoerPsd = "effect_bug.psd";
string uitvoerPng = "effect_bug.png";

using (var psdAfbeelding = new PsdImage(500, 500))
{
    // Tekstlagen toevoegen
    Aspose.PSD.Rectangle tekstGebied1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle tekstGebied2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle tekstGebied3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer tekstLaag1 = psdAfbeelding.AddTextLayer("Tekst Met Effecten", tekstGebied1);
    TextLayer tekstLaag2 = psdAfbeelding.AddTextLayer("Tekst Met Effecten", tekstGebied2);
    TextLayer tekstLaag3 = psdAfbeelding.AddTextLayer("Tekst Met Effecten", tekstGebied3);

    // Tekstlagen aanpassen
    tekstLaag1.TekstGegevens.Items[0].Stijl.Lettergrootte = 150;
    tekstLaag1.TekstGegevens.Items[0].Stijl.VulKleur = Aspose.PSD.Color.Goldenrod;
    tekstLaag1.TekstGegevens.WerkLaagGegevensBij();

    tekstLaag2.TekstGegevens.Items[0].Stijl.Lettergrootte = 150;
    tekstLaag2.TekstGegevens.Items[0].Stijl.VulKleur = Aspose.PSD.Color.Goldenrod;
    tekstLaag2.TekstGegevens.WerkLaagGegevensBij();

    tekstLaag3.TekstGegevens.Items[0].Stijl.Lettergrootte = 150;
    tekstLaag3.TekstGegevens.Items[0].Stijl.VulKleur = Aspose.PSD.Color.Goldenrod;
    tekstLaag3.TekstGegevens.WerkLaagGegevensBij();

    // Effecten toevoegen
    OuterGlowEffect gloed = tekstLaag1.MengOpties.AddOuterGlow(); // verbreken
    gloed.Verspreiding = 15;
    ((ColorFillSettings)gloed.VulKleur).Kleur = Color.Rood;

    var schaduw = tekstLaag2.MengOpties.AddDropShadow(); // verbreken met lange tekst
    schaduw.Afstand = 25;
    schaduw.Kleur = Color.Donkerblauw;

    var binnenSchaduw = tekstLaag3.MengOpties.AddInnerShadow(); // verbreken met lange tekst
    binnenSchaduw.GebruikGlobaalLicht = false;
    binnenSchaduw.Hoek = -179;
    binnenSchaduw.Afstand = 10;
    binnenSchaduw.Grootte = 8;
    binnenSchaduw.Kleur = Color.HotPink;

    // exporteren
    psdAfbeelding.Save(uitvoerPsd);
    psdAfbeelding.Save(uitvoerPng, new PngOpties() { KleurType = Aspose.PSD.Bestandsindelingen.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}