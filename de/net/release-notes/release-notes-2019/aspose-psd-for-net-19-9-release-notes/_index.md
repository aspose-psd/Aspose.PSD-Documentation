---
title: Aspose.PSD für .NET 19.9 - Versionshinweise
type: docs
weight: 40
url: /de/net/aspose-psd-für-net-19-9-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-160|Falscher Ebenenname extrahiert|Funktion|
|PSDNET-175|Abrufen von Texteigenschaften aus einem anderen Textabschnitt innerhalb der PSD-Textebene|Funktion|
|PSDNET-190|Unterstützung für Hinzufügen von Ebenengruppe|Funktion|
|PSDNET-192|Unterstützung der Skaleneigenschaft für Füllgradientenebene|Funktion|
|PSDNET-162|Helligkeit anpassen|Verbesserung|
|PSDNET-174|IndexOutOfRangeException beim Speichern von PSD-Bild als JPEG|Fehler|
|PSDNET-180|Aktualisieren des Textebenen-Texts wirft eine Ausnahme|Fehler|
|PSDNET-182|Speichern eines PSD-Bildes nach RotateFlip-Operation erzeugt eine beschädigte Datei, die nicht geöffnet werden kann|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **Entfernte APIs:**
- Keine

## **Verwendungsbeispiele:**
**PSDNET-160. Falscher Ebenenname extrahiert**

Um den Ebenennamen korrekt anzuzeigen, verwenden Sie die **DisplayName**-Eigenschaft. Es wurde ein Setter für diese Eigenschaft hinzugefügt, und die Eigenschaft kann geändert werden. Wenn Photoshop beim Speichern des Ebenennamens die Name-Eigenschaft verwendet, werden koreanische Zeichen als Byte 63 '?' in ASCII gespeichert. Verwenden Sie die **DisplayName**-Eigenschaft, da die Name-Eigenschaft koreanische Zeichen nicht unterstützt.

{{< highlight java >}}

// Änderungen an den Ebenennamen vornehmen und speichern

using (var image = (PsdImage)Image.Load("EbenenMitNamen.psd"))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // neuen Wert in DisplayName-Eigenschaft setzen

        layer.DisplayName += "_geändert";

    }

    image.Save("ausgabe.psd");

}

{{< /highlight >}}

**PSDNET-175. Abrufen von Texteigenschaften aus einem anderen Textabschnitt innerhalb der PSD-Textebene**

{{< highlight java >}}

const double Toleranz = 0.0001;

var dateipfad = "DreiFarbenAbschnitte.psd";

var ausgabepfad = "DreiFarbenAbschnitte_aus.psd";

using (var im = (PsdImage)Image.Load(dateipfad))

{

    for (int i = 0; i < im.Layers.Length; i++)

    {

        var ebene = im.Layers[i] as TextLayer;

        if (ebene != null)

        {

            var abschnitte = ebene.TextData.Items;

            if (abschnitte.Length != 4)

            {

                throw new Exception();

            }

            // Texte jedes Abschnitts überprüfen

            if (abschnitte[0].Text != "Alt " ||

                abschnitte[1].Text != "Farbe" ||

                abschnitte[2].Text != " Text\r" ||

                abschnitte[3].Text != "Zweiter Absatz\r")

            {

                throw new Exception();

            }

            // Absatzdaten überprüfen

            // Absätze haben unterschiedliche Ausrichtung

            if (

                abschnitte[0].Paragraph.Justification != 0 ||

                abschnitte[1].Paragraph.Justification != 0 ||

                abschnitte[2].Paragraph.Justification != 0 ||

                abschnitte[3].Paragraph.Justification != 2)

            {

                throw new Exception();

            }

            // Alle anderen Eigenschaften des ersten und zweiten Absatzes sind gleich

            for (int j = 0; j < abschnitte.Length; j++)

            {

                var absatz = abschnitte[j].Paragraph;

                if (Math.Abs(absatz.AutoLeading - 1.2) > Toleranz ||

                    absatz.AutoHyphenate != false ||

                    absatz.Burasagari != false ||

                    absatz.ConsecutiveHyphens != 8 ||

                    Math.Abs(absatz.StartIndent) > Toleranz ||

                    Math.Abs(absatz.EndIndent) > Toleranz ||

                    absatz.EveryLineComposer != false ||

                    Math.Abs(absatz.FirstLineIndent) > Toleranz ||

                    absatz.GlyphSpacing.Length != 3 ||

                    Math.Abs(absatz.GlyphSpacing[0] - 1) > Toleranz ||

                    Math.Abs(absatz.GlyphSpacing[1] - 1) > Toleranz ||

                    Math.Abs(absatz.GlyphSpacing[2] - 1) > Toleranz ||

                    absatz.Hanging != false ||

                    absatz.HyphenatedWordSize != 6 ||

                    absatz.KinsokuOrder != 0 ||

                    absatz.LetterSpacing.Length != 3 ||

                    Math.Abs(absatz.LetterSpacing[0]) > Toleranz ||

                    Math.Abs(absatz.LetterSpacing[1]) > Toleranz ||

                    Math.Abs(absatz.LetterSpacing[2]) > Toleranz ||

                    absatz.LeadingType != LeadingMode.Auto ||

                    absatz.PreHyphen != 2 ||

                    absatz.PostHyphen != 2 ||

                    Math.Abs(absatz.SpaceBefore) > Toleranz ||

                    Math.Abs(absatz.SpaceAfter) > Toleranz ||

                    absatz.WordSpacing.Length != 3 ||

                    Math.Abs(absatz.WordSpacing[0] - 0.8) > Toleranz ||

                    Math.Abs(absatz.WordSpacing[1] - 1.0) > Toleranz ||

                    Math.Abs(absatz.WordSpacing[2] - 1.33) > Toleranz ||

                    Math.Abs(absatz.Zone - 36.0) > Toleranz)

                {

                    throw new Exception();

                }

            }

            // Stildaten überprüfen

            // Stile haben unterschiedliche Farben und Schriftgröße

            if (Math.Abs(abschnitte[0].Style.FontSize - 12) > Toleranz ||

                Math.Abs(abschnitte[1].Style.FontSize - 12) > Toleranz ||

                Math.Abs(abschnitte[2].Style.FontSize - 12) > Toleranz ||

                Math.Abs(abschnitte[3].Style.FontSize - 10) > Toleranz)

            {

                throw new Exception();

            }

            if (abschnitte[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                abschnitte[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                abschnitte[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                abschnitte[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

            {

                throw new Exception();

            }

            for (int j = 0; j < abschnitte.Length; j++)

            {

                var stil = abschnitte[j].Style;

                if (stil.AutoLeading != false ||

                    stil.HindiNumbers != false ||

                    stil.Kerning != 0 ||

                    stil.Leading != 0 ||

                    stil.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                    stil.Tracking != 50)

                {

                    throw new Exception();

                }

            }

            // Beispiel für Textbearbeitung

            abschnitte[0].Text = "Hallo ";

            abschnitte[1].Text = "Welt";

            // Beispiel für Entfernen von Textabschnitten

            ebene.TextData.RemovePortion(3);

            ebene.TextData.RemovePortion(2);

            // Beispiel für Hinzufügen eines neuen Textabschnitts

            var erstellterAbschnitt = ebene.TextData.ProducePortion();

            erstellterAbschnitt.Text = "!!!\r";

            ebene.TextData.AddPortion(erstellterAbschnitt);

            abschnitte = ebene.TextData.Items;

            // Beispiel für Bearbeiten von Absatz und Stil für Abschnitte

            // Richtige Ausrichtung festlegen

            abschnitte[0].Paragraph.Justification = 1;

            abschnitte[1].Paragraph.Justification = 1;

            abschnitte[2].Paragraph.Justification = 1;

            // Unterschiedliche Farben für jeden Stil. Diese werden geändert, aber die Darstellung wird nicht vollständig unterstützt

            abschnitte[0].Style.FillColor = Color.Aquamarin;

            abschnitte[1].Style.FillColor = Color.Violett;

            abschnitte[2].Style.FillColor = Color.Hellblau;

            // Unterschiedliche Schriftart. Diese werden geändert, aber die Darstellung wird nicht vollständig unterstützt

            abschnitte[0].Style.FontSize = 6;

            abschnitte[1].Style.FontSize = 8;

            abschnitte[2].Style.FontSize = 10;

            ebene.TextData.UpdateLayerData();

            im.Save(ausgabepfad, new PsdOptions(im));

            break;

        }

    }

}

{{< /highlight >}}

**PSDNET-190. Unterstützung für Hinzufügen von Ebenengruppe**

{{< highlight java >}}

// -Gruppe 1

// --Ebene 1

// --Gruppe 2

// ---Ebene 2

// ---Ebene 3

// --Ebene 4

string datenverzeichnis = "psdnet190_test.psd";

var createOptions = new PsdOptions();

createOptions.Source = new FileCreateSource(datenverzeichnis, false);

createOptions.Palette = new PsdColorPalette(new Color[] { Color.Green });

using (var psdImage = (PsdImage)Image.Create(createOptions, 500, 500))

{

    LayerGroup gruppe1 = psdImage.AddLayerGroup("Gruppe 1", 0, true);

    Layer ebene1 = new Layer(psdImage);

    ebene1.Name = "Ebene 1";

    gruppe1.AddLayer(ebene1);

    LayerGroup gruppe2 = gruppe1.AddLayerGroup("Gruppe 2", 1);

    Layer ebene2 = new Layer(psdImage);

    ebene2.Name = "Ebene 2";

    gruppe2.AddLayer(ebene2);

    Layer ebene3 = new Layer(psdImage);

    ebene3.Name = "Ebene 3";

    gruppe2.AddLayer(ebene3);

    Layer ebene4 = new Layer(psdImage);

    ebene4.Name = "Ebene 4";

    gruppe1.AddLayer(ebene4);

    psdImage.Save();

}

{{< /highlight >}}

**PSDNET-192. Unterstützung der Skaleneigenschaft für Füllgradientenebene**

{{< highlight java >}}

using (var image = (PsdImage)Image.Load("Füllgradientenebene.psd"))

{

    // Füllebene abrufen

    FillLayer füllebene = null;

    foreach (var ebene in image.Layers)

    {

        füllebene = ebene as FillLayer;

        if (füllebene != null)

        {

            break;

        }

    }

    var einstellungen = füllebene.FillSettings as IGradientFillSettings;

    // Skalenwert aktualisieren

    einstellungen.Scale = 200;

    füllebene.Update(); // Aktualisiert Pixel-Daten

    image.Save("skaliertesBild.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}



**PSDNET-174. IndexOutOfRangeException beim Speichern von PSD-Bild als JPEG**

{{< highlight java >}}

         using (var image = Aspose.PSD.Image.Load("BeispielPSD.psd"))

        {

            image.Save("beispielJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. Aktualisieren des Textebenen-Texts wirft eine Ausnahme**

{{< highlight java >}}

           // Akt