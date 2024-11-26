---
title: Aspose.PSD voor .NET 18.10 - Release-opmerkingen
type: docs
weight: 30
url: /nl/net/aspose-psd-voor-net-18-10-release-opmerkingen/
---

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-14|Ondersteuning toevoegen van mengmodi naast Normaal|Functie|
|PSDNET-69|Ondersteuning toevoegen van Kleur Overlay-effect|Functie|
|PSDNET-70|Ondersteuning toevoegen van Schaduw-effect|Functie|
|PSDNET-71|Rendering voor exporteren van Kleur Overlay-effect|Functie|
|PSDNET-72|Rendering voor exporteren van Schaduw-effect|Functie|
|PSDNET-74|Ondersteuning toevoegen van Laageffecten tijdens runtime|Functie|
|PSDNET-73|Optimaliseren van laadprestaties van bronnen die osTypeStructure bevatten|Fout|
|PSDNET-79|Refactoring en geheugenlekfixes in LayerAndMaskInfo|Verbetering|

## **Gebruik voorbeelden:**
**PSDNET-14 Ondersteuning toevoegen van mengmodi naast Normaal**

{{< highlight java >}}

 var bestanden = new string[]

{

    "Normaal",

    "Oplossen",

    "Verduisteren",

    "Vermenigvuldigen",

    "Kleur Doordrukken",

    "Lineair Doordrukken",

    "Donkerder Kleur",

    "Lichter",

    "Scherm",

    "Kleur Doordrukken",

    "Lineair Doordrukken Toevoegen",

    "Lichtere Kleur",

    "Overlay",

    "Zacht Licht",

    "Hard Licht",

    "Duidelijk Licht",

    "Lineair Licht",

    "Pinlicht",

    "Hard Mix",

    "Verschil",

    "Uitsluiting",

    "Aftrekken",

    "Verdelen",

    "Tint",

    "Verzadiging",

    "Kleur",

    "Luminantie",

};

foreach (var bestandsnaam in bestanden)

{

    using (var afbeelding = LaadBestand(bestandsnaam + ".psd"))

    {

        // Exporteer naar PNG

        var opslagOpties = new PngOpties();

        opslagOpties.Kleurtype = PngKleurtype.TrueColorMetAlpha;

        var pngExportPad100 = "Mengmodus" + bestandsnaam + "_Test100.png";

        afbeelding.Opslaan(pngExportPad100, opslagOpties);

        // Zet de dekking op 50%

        afbeelding.Lagen[1].Dekking = 127;

        var pngExportPad50 = "Mengmodus" + bestandsnaam + "_Test50.png";

        afbeelding.Opslaan(pngExportPad50, opslagOpties);

    }

}

{{< /highlight >}}

**PSDNET-69 Ondersteuning toevoegen van Kleur Overlay-effect**

{{< highlight java >}}

     // Bewerken van Kleur Overlay-effect

    string bronBestandsnaam = "KleurOverlay.psd";

    string psdPadNaWijziging = "KleurOverlayGewijzigd.psd";

    using (var afbeelding = LaadBestand(bronBestandsnaam))

    {

       var kleurOverlay = (KleurOverlay)(afbeelding.Lagen[1].Mengingsopties.Effecten[0]);



       Assert.AreEqual(Kleur.Rood, kleurOverlay.Kleur);

       Assert.AreEqual(153, kleurOverlay.Dekking);

       kleurOverlay.Kleur = Kleur.Groen;

       kleurOverlay.Dekking = 128;

       afbeelding.Opslaan(psdPadNaWijziging);

    }

{{< /highlight >}}

**PSDNET-70 Ondersteuning toevoegen van Schaduw-effect**

{{< highlight java >}}

     // Bewerken van Schaduweffect

    string bronBestandsnaam = "Schaduw.psd";

    string psdPadNaWijziging = "SchaduwGewijzigd.psd";

    using (var afbeelding = LaadBestand(bronBestandsnaam))

    {

       var schaduweffect = (SchaduwEffect)(afbeelding.Lagen[1].Mengingsopties.Effecten[0]);



       Assert.AreEqual(Kleur.Zwart, schaduweffect.Kleur);

       Assert.AreEqual(255, schaduweffect.Dekking);

       Assert.AreEqual(3, schaduweffect.Afstand);

       Assert.AreEqual(7, schaduweffect.Grootte);

       Assert.AreEqual(true, schaduweffect.GebruikGlobaalLicht);

       Assert.AreEqual(90, schaduweffect.Hoek);

       Assert.AreEqual(0, schaduweffect.Spreiding);

       Assert.AreEqual(0, schaduweffect.Ruis);

       schaduweffect.Kleur = Kleur.Groen;

       schaduweffect.Dekking = 128;

       schaduweffect.Afstand = 11;

       schaduweffect.GebruikGlobaalLicht = false;

       schaduweffect.Grootte = 9;

       schaduweffect.Hoek = 45;

       schaduweffect.Spreiding = 3;

       schaduweffect.Ruis = 50;

       afbeelding.Opslaan(psdPadNaWijziging);

    }

{{< /highlight >}}



**PSDNET-71 Rendering voor exporteren van Kleur Overlay-effect**

{{< highlight java >}}

    // Bewerken van Kleur Overlay-effect

    string bronBestandsnaam = "KleurOverlay.psd";

    string pngExportPad = "KleurOverlay.png";

    using (var afbeelding = LaadBestand(bronBestandsnaam))

    {

       var kleurOverlay = (KleurOverlayEffect)(afbeelding.Lagen[1].Mengingsopties.Effecten[0]);



       Assert.AreEqual(Kleur.Rood, kleurOverlay.Kleur);

       Assert.AreEqual(153, kleurOverlay.Dekking);

       // Opslaan als PNG

       var opslagOpties = new PngOpties();

       opslagOpties.Kleurtype = PngKleurtype.TrueColorMetAlpha;

       afbeelding.Opslaan(pngExportPad, opslagOpties);

    }

{{< /highlight >}}

**PSDNET-72 Rendering voor exporteren van Schaduw-effect**

{{< highlight java >}}

     // Exporteren van Schaduw

    string bronBestandsnaam = "Schaduw.psd";

    string pngExportPad = "Schaduw.png";

    using (var afbeelding = LaadBestand(bronBestandsnaam))

    {

       var schaduweffect = (SchaduwEffect)(afbeelding.Lagen[1].Mengingsopties.Effecten[0]);



       Assert.AreEqual(Kleur.Zwart, schaduweffect.Kleur);

       Assert.AreEqual(255, schaduweffect.Dekking);

       Assert.AreEqual(3, schaduweffect.Afstand);

       Assert.AreEqual(7, schaduweffect.Grootte);

       Assert.AreEqual(true, schaduweffect.GebruikGlobaalLicht);

       Assert.AreEqual(90, schaduweffect.Hoek);

       Assert.AreEqual(0, schaduweffect.Spreiding);

       Assert.AreEqual(0, schaduweffect.Ruis);

       // Opslaan als PNG

       var opslagOpties = new PngOpties();

       opslagOpties.Kleurtype = PngKleurtype.TrueColorMetAlpha;

       afbeelding.Opslaan(pngExportPad, opslagOpties);

    }

{{< /highlight >}}

**PSDNET-74 Ondersteuning van het toevoegen van laageffecten tijdens runtime**

{{< highlight java >}}

     // Kleur-overlay laageffect toevoegen tijdens runtime

    string bronBestandsnaam = "DrieReguliereLagenMetLaageffecten.psd";

    string psdExportPad = "DrieReguliereLagenMetLaageffectenGewijzigd.psd";

    string pngExportPad = "DrieReguliereLagenMetLaageffectenGewijzigd.psd";

    var laadOpties = new PsdLaadOpties()

    {

        LaadEffectenBron = true

    };



    var testMap = string.Empty;

    var afbeelding = (PsdAfbeelding)Afbeelding.Laad(testPad, laadOpties) 

    using (afbeelding)

    {

        var effect = afbeelding.Lagen[1].Mengingsopties.KleurOverlayToevoegen();

        effect.Dekking = 128;

        effect.Kleur = Kleur.Groen;

        effect.Mengmodus = Mengmodus.Normaal;

        var effect = afbeelding.Lagen[1].Mengingsopties.SchaduwToevoegen();

        effect.Kleur = Kleur.Rood;

        effect.Dekking = 128;

        effect.Mengmodus = Mengmodus.Normaal;



        // Opslaan als PSD    

        afbeelding.Opslaan(psdExportPad);



        // Opslaan als PNG

        var opslagOpties = new PngOpties();

        afbeelding.Opslaan(pngExportPad, opslagOpties);

    }

{{< /highlight >}}
