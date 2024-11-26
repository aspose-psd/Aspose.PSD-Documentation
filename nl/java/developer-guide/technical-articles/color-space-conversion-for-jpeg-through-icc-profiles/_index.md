---
title: Kleurruimteconversie voor JPEG via ICC-profielen
type: docs
weight: 50
url: /nl/java/kleurruimteconversie-voor-jpeg-via-icc-profielen/
---

## **Kleurbeheer voor JPEG-indeling**

Dit artikel bespreekt het gebruik van ICC-profielen om kleurruimtemanagement uit te voeren tijdens het verwerken van JPEG-indeling met Aspose.PSD API's. De binnenste kleurruimte van JPEG is YCbCr, maar deze indeling kan ook Grijswaarde, RGB, CMYK en YCCK-kleurruimtes herbergen om de metadata van de afbeelding op te slaan. Aspose.PSD API's werken voornamelijk in de RGB-ruimte. Daarom moet de API kleurruimteconversies van en naar uitvoeren om JPEG-bestanden op de juiste manier te verwerken. Grijswaarde naar RGB en YCbCr naar RGB conversies kunnen worden gedaan met wiskundige transformaties, maar CMYK- en YCCK-ruimtes kunnen niet eenvoudig naar RGB-ruimte worden geconverteerd.

De Aspose.PSD API's moeten directe RGB naar CMYK-kleurtransformatie uitvoeren voor JPEG-afbeeldingen met CMYK-kleurruimte. Aan de andere kant vereisen afbeeldingen met YCCK-kleurruimte RGB naar CMYK naar YCCK-kleurtransformatie, waarbij de CMYK naar YCCK-transformatie de ITU-R BT.601-conversie gebruikt die wordt toegepast op de eerste drie kanalen, waarbij het kanaal k onaangeroerd blijft. Kortom, Aspose.PSD API's moeten kleurruimte-interconversie uitvoeren van RGB en CMYK-kleurruimtes voor zowel CMYK- als YCCK-afbeeldingen, en dergelijke transformaties worden uitgevoerd met behulp van ICC-profielen die in feite zoektabellen zijn die de eigenschappen van een kleur beschrijven en helpen bij de kleurtransformaties.

## **ICC-profielen**
Het ICC-conversiemechanisme gebruikt "Profielen" die de bronkleurruimte toewijzen aan apparaatonafhankelijke CIELAB- of CIEXYZ-kleurruimtes. Aspose.PSD kan gegevens converteren naar de kleurruimte zoals vereist door deze twee kleurruimtes met aanvullende profielen te gebruiken. Daarom moet de gebruiker voor ICC-conversie twee profielen leveren - één RGB-profiel om naar de innerlijke CIE-kleurruimte te komen en één CMYK-profiel om de CMYK-kleureigenschappen te verkrijgen. Om de CMYK naar RGB conversie te bereiken, moet men profielen omwisselen, dat wil zeggen; het CMYK-profiel als bronprofiel gebruiken en het RGB-profiel als bestemmingsprofiel.

## **Kleurconversie voor JPEG via ICC-profielen**
Aspose.PSD API's verbergen de details en bieden een eenvoudig te gebruiken mechanisme om ICC-profielen te specificeren via de JpegOptions-klasse. Bovendien gebruikt Aspose.PSD de voorbeeldprofielen van SWOP CMYK en sRGB die in de kern zijn ingebed, dus in de meest gebruikelijke gevallen hoeft de gebruiker niet te zoeken naar specifieke profielen. Er is een nadeel aan dergelijke correcties, namelijk; dergelijke kleurruimteconversies zijn onomkeerbaar omdat we niet kunnen verwachten dezelfde kleur te verkrijgen na RGB naar CMYK naar RGB conversie vanwege incompatibele kleurruimtes en verschillende kleurprofielen. Het volgende codefragment demonstreert het gebruik van Aspose.PSD voor de Java-API om RGB- en CMYK-kleurprofielen voor een YCCK JPEG-afbeelding te specificeren. In het onderstaande voorbeeld worden RGB- en CMYK-kleurprofielen gewijzigd en wordt de afbeelding opgeslagen in de YCCK-kleurruimte. Let op dat die RgbColorProfile- en CmykColorProfile-eigenschappen werken voor het wijzigen van pixelgegevens voor de YCCK-kleurruimte. Alle andere kleurruimtes halen geen kleurprofielen op voor het bijwerken van de kleurgegevens.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}

Als er geen profielen zijn ingesteld, zal Aspose.PSD voor de Java-API standaardprofielen gebruiken. Het volgende voorbeeld gebruikt eigenschappen van bestemmingsprofielen die de bestemmingskleurruimte wijzigen voor de meeste Jpeg-afbeeldingen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}
