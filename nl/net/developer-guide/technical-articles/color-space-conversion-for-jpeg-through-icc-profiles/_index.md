---
title: Kleurruimteconversie voor JPEG via ICC-profielen
type: docs
weight: 60
url: /nl/kleurruimteconversie-voor-jpeg-via-icc-profielen/
---

## **Kleurbeheer voor JPEG-indeling**

Dit artikel bespreekt het gebruik van ICC-profielen om kleurruimtebeheer uit te voeren bij het omgaan met JPEG-indeling met behulp van de Aspose.PSD API's. De innerlijke kleurruimte van JPEG is YCbCr, echter kan deze [indeling](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) ook grijswaarden, RGB, CMYK en YCCK kleurruimten herbergen om de metagegevens van de afbeelding op te slaan. Aspose.PSD API's werken hoofdzakelijk in de RGB-ruimte, daarom moet de API conversies van en naar kleurruimten uitvoeren om JPEG-bestanden op de juiste manier te kunnen verwerken. Conversies van grijsschaal naar RGB en van YCbCr naar RGB kunnen worden gedaan met wiskundige transformaties, maar CMYK- en YCCK-ruimten kunnen niet eenvoudig naar de RGB-ruimte worden omgezet.

De Aspose.PSD API's moeten directe RGB-naar-CMYK-kleurtransformatie uitvoeren voor JPEG-afbeeldingen met CMYK-kleurruimte. Aan de andere kant vereisen afbeeldingen met YCCK-kleurruimte RGB-naar-CMYK-naar-YCCK kleurtransformatie, waarbij de CMYK-naar-YCCK-transformaie gebruikmaakt van de [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601)-conversie die wordt toegepast op de eerste drie kanalen, waarbij het kanaal k onaangeroerd blijft. Kortom, Aspose.PSD API's moeten onderlinge conversies van RGB en CMYK kleurruimten uitvoeren voor zowel CMYK- als YCCK-afbeeldingen, en dergelijke transformaties worden uitgevoerd met behulp van ICC-profielen die in feite tabelwaarden beschrijven die de eigenschappen van een kleur beschrijven en helpen bij de kleurtransformaties.

## **ICC-profielen**
Het ICC-conversiemechanisme gebruikt "Profielen" die de bronkleurruimte toewijzen aan een apparaatonafhankelijke CIELAB- of CIEXYZ-kleurruimte. Aspose.PSD kan gegevens converteren naar de vereiste kleurruimte met behulp van deze twee kleurruimten met aanvullende profielen. Daarom moet de gebruiker voor ICC-conversie twee profielen verstrekken - een RGB-profiel om naar de interne CIE-kleurruimte te gaan en een CMYK-profiel om de CMYK-kleurkarakteristieken te verkrijgen. Om de CMYK-naar-RGB-conversie te bereiken, moet men profielen omwisselen, dat wil zeggen; het CMYK-profiel als bronprofiel gebruiken en het RGB-profiel als bestemmingsprofiel.

## **Kleurconversie voor JPEG via ICC-profielen**
Aspose.PSD API's verbergen de details en bieden een eenvoudig te gebruiken mechanisme om ICC-profielen te specificeren via de [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)-klasse. Bovendien gebruikt Aspose.PSD de standaardprofielen van SWOP, CMYK en sRGB die zijn ingesloten in de kern ervan, daarom hoeft de gebruiker in de meeste gebruikelijke gevallen niet te zoeken naar specifieke profielen. Er is een nadeel van dergelijke correcties, namelijk; dergelijke kleurruimteconversies zijn onomkeerbaar omdat we niet dezelfde kleur kunnen verwachten na RGB-naar-CMYK-naar-RGB-conversie vanwege incompatibele kleurruimten en verschillende kleurprofielen. De volgende codefragment demonstreert het gebruik van Aspose.PSD voor .NET API om RGB- en CMYK-kleurprofielen voor YCCK-JPEG-afbeelding te specificeren. In het onderstaande voorbeeld worden RGB- en CMYK-kleurprofielen gewijzigd en wordt de afbeelding opgeslagen in de YCCK-kleurruimte. Let op dat deze [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile)- en [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile)-eigenschappen werken voor het wijzigen van pixelgegevens voor de YCCK-kleurruimte. Alle andere kleurruimten halen geen kleurprofielen op voor het bijwerken van de kleurgegevens.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Als er geen profielen zijn ingesteld, zal Aspose.PSD voor .NET API de standaardprofielen gebruiken. Het onderstaande voorbeeld gebruikt eigenschappen van de bestemmingsprofielen die de bestemmingskleurruimte wijzigen voor de meeste JPEG-afbeeldingen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
