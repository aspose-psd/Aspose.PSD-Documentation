---
title: Rasterlaagmaskers bewerken in een PSD-bestand via API
type: docs
weight: 20
url: /nl/bewerken-van-rasterlaagmaskers-in-psd-bestand-via-api/
---

## **Overzicht**
**Om PSD-opmaak te automatiseren en een PSD-bestand te wijzigen zonder Adobe® Photoshop® te gebruiken, kunt u de onderstaande Aspose.PSD API gebruiken. Er zijn C# en .NET codefragmenten die u kunnen helpen bij het aanpassen van PSD-bestanden.**

Met behulp van PSD Laag- en Vectormaskers kunnen we laagpixels verbergen en weergeven zonder ze permanent te verwijderen. Rastermaskers worden ook wel laagmaskers of gebruikersmaskers genoemd. Toegang tot zowel raster- als vectormaskers in Aspose.PSD wordt geboden via de [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) laageigenschap, die een instantie kan zijn van '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' en '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' klassen die kindklassen zijn van de abstracte 'LayerMaskData' klasse. Als een laag zowel raster- als vectormaskers heeft, wordt een instantie van [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)geleverd. Als een laag slechts een raster- of een vectormasker heeft, wordt een instantie van [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)geleverd. Als de LayerMaskData-eigenschap null is, heeft de laag geen maskers of alleen een uitgeschakeld vectormasker.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Een rastermasker en een uitgeschakeld vectormasker LayerMaskDataShort</p><p>Een uitgeschakeld rastermasker LayerMaskDataShort</p><p>Een rastermasker en een vectormasker LayerMaskDataFull</p><p>Een rastermasker LayerMaskDataShort</p><p>Een vectormasker LayerMaskDataShort</p><p>Een uitgeschakeld vectormasker null (Maar vector resource is aanwezig)</p>|
| :- | :- |
## **Hoe krijg je een laagrastermasker in het PSD-bestand?**
Als eerste moeten we uitzoeken of een laag zowel vectormaskers als laagmaskers heeft:

Hieronder wordt aan de hand van een voorbeeldcode gedemonstreerd hoe je een laagrastermasker kunt verkrijgen

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Als de LayerMaskData-laageigenschap van het type LayerMaskDataShort is. In dat geval, laten we controleren of de laag alleen een rastermasker heeft door de Flags-eigenschap te controleren. Deze mag de [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** vlag niet bevatten, anders is het masker een vectormaskerbuffer**.**

Codefragment voor het verkrijgen van een masker:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Als je een rastermasker moet **extraheren** als LayerMaskDataShort (voor verdere manipulaties), zelfs als beide maskers aanwezig zijn, moet LayerMaskDataFull worden geëxtraheerd en geconverteerd naar LayerMaskDataShort. De volgende code kan worden gebruikt voor beide gevallen:

Een rastermasker uit PSD extraheren

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **Hoe controleer je of een laag in het PSD-bestand een rastermasker heeft?**
De volgende C#-code kan je helpen controleren of een laag een rastermasker heeft:

Hoe te weten of rastermasker is toegepast op [PSD Laag](/psd/nl/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **Hoe verwijderen / toevoegen / bijwerken van een laagrastermasker in het PSD-bestand?**
Het verwijderen / toevoegen / bijwerken van alleen LayerMaskData is niet voldoende voor correcte opslag omdat kanalen niet worden bijgewerkt; hoewel het mogelijk correcte rendering geeft. Dit verandert de maskerkanalen niet:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

We moeten de laag AddLayerMask-methode gebruiken voor het verwijderen / toevoegen / bijwerken.

Hiermee worden zowel het masker als de kanalen toegevoegd/ bijgewerkt:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Hiermee worden zowel het masker als de kanalen verwijderd:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **Een laagrastermasker verwijderen in de PSD-afbeelding**
Allereerst controleren we of het masker in het kort formaat staat en als het geen vectormasker is, kunnen we gewoon de AddLayerMask-methode met null aanroepen om het rastermasker te verwijderen. Maar als het in het volledige formaat staat, moeten we het converteren naar een kort formaat zodat alleen het vectormasker overblijft. Voor het verwijderen van een laagmasker kan het volgende C# .NET-codefragment worden gebruikt:

Codefragment hoe een Laagmasker te verwijderen uit een PSD-bestand.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **Een laagrastermasker bijwerken in de PSD-afbeelding**
Dit is eenvoudig: als het masker in het kort formaat staat, moeten we ImageData en MaskRectangle wijzigen indien nodig, anders moeten [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)en [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)worden gewijzigd. Het volgende C# .NET-codefragment kan worden gebruikt voor het bijwerken van een laagmasker:

PSD Laagmasker bijwerken met C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Hier is een voorbeeld van mogelijke acties die een rastermasker veranderen. Deze keert een laaggebruikersmasker om:

PSD Laagmasker bijwerken met C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **Een vectormasker bijwerken in het PSD-bestand wanneer een laagrastermasker aanwezig is**
Het wordt verondersteld dat een gebruiker al een vectortrajectbron heeft gewijzigd. Dan kan het vectormasker eenvoudig worden bijgewerkt door de [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask)laagmethode aan te roepen:

PSD Laagvectormasker bijwerken met C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **Een laagrastermasker toevoegen in het PSD-bestand**
Als een laag geen masker heeft, kunnen we het opgegeven rastermasker eenvoudig toevoegen door de AddLayerMask laagmethode aan te roepen.

Als het masker geen [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)vlag heeft dan heeft het al een rastermasker en moeten we het bijwerken zoals hierboven beschreven. Anders, als dit masker in een kort formaat staat, converteren we het naar het volledige formaat. Als dat niet het geval is, gebruiken we het zoals het is. Vervolgens bijwerken van UserMaskData, UserMaskRectangle en andere eigenschappen met de gegeven maskereigenschappen. Het volgende C# .NET-codefragment kan worden gebruikt voor het toevoegen (bijwerken) van een laagmasker:

Nieuw Laagmasker toevoegen aan PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Hoe controleren of een laagmasker is ingeschakeld?**
Om de ingeschakelde status van een laagrastermasker te achterhalen, kunnen we de staat van de LayerMaskFlags.Disabled-vlag controleren in de Flags-eigenschap voor LayerMaskDataShort of in de RealFlags voor LayerMaskDataFull. Het volgende C# .NET-codefragment kan worden gebruikt om de ingeschakelde status van een laagmasker te krijgen:

Controleren of een masker is ingeschakeld:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **Hoe een rasterlaagmasker in-of uitschakelen?**
Om een laagrastermasker in- of uit te schakelen kunnen we de staat van de LayerMaskFlags.Disabled-vlag wijzigen in de Flags-eigenschap voor LayerMaskDataShort of in de RealFlags voor LayerMaskDataFull. Het volgende C# .NET-codefragment kan worden gebruikt om de ingeschakelde status van een laagmasker te wijzigen:

Rasterlaagmasker in- of uitschakelen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
