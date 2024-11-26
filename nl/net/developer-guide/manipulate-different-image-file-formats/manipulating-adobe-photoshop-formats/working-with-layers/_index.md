---
title: Werken met Lagen
type: docs
weight: 150
url: /nl/werken-met-lagen/
---

## **Een Laaggroep Maken**
Een laaggroep bestaat uit één of meer lagen en het helpt bij het organiseren van vergelijkbare of gerelateerde lagen. Met Aspose.PSD voor .NET kunt u een laaggroep maken. Hiervoor is een nieuwe methode [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) toegevoegd aan de **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** klasse om de laaggroep toe te voegen.

De stappen om laaggroepen te maken zijn als volgt:

- Maak een instantie van een afbeelding met de PsdImage klasse met de gespecificeerde breedte, hoogte en afbeeldingsopties.
- Maak een [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) met de gespecificeerde groepsnaam en index.
- Maak een instantie van de Layer klasse en wijs de PSD-afbeelding eraan toe.
- Voeg de gemaakte laag toe aan de laaggroep met behulp van de AddLayer methode die wordt blootgesteld door de LayerGroup klasse.
- Sla de resultaten op.

De volgende codefragment laat zien hoe u een laaggroep kunt maken.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Een Laag Hernoemen**
U kunt elke naam gebruiken die u maar wilt, maar de gebruikelijke praktijk is om een algemene beschrijving te geven van het object of element dat op die laag staat. In dit artikel wordt gedemonstreerd hoe u de naam van een laag kunt wijzigen met behulp van Aspose.PSD voor .NET. Hiervoor is een nieuwe eigenschap [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) toegevoegd aan de Layer klasse om een laagnaam correct weer te geven. Het is waargenomen dat wanneer Photoshop een laagnaam opslaat met behulp van de **Name** eigenschap, dan worden Koreaanse karakters opgeslagen als byte 63'?' in ASCII. Dus, als u een laagnaam correct wilt weergeven, gebruik dan de **DisplayName** eigenschap omdat de **Name** eigenschap geen Koreaanse tekens ondersteunt.

Het volgende codevoorbeeld laat zien hoe u een laag kunt hernoemen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Ondersteuning van Gekoppelde Lagen**
Het koppelen van lagen is vergelijkbaar met het groeperen van lagen. Als u twee of meer lagen koppelt, kunt u bepaalde wijzigingen aanbrengen in beide gekoppelde lagen. Bijvoorbeeld, als u transformaties toepast op één laag, worden deze toegepast op alle andere gekoppelde lagen. Dit artikel laat zien hoe u gekoppelde lagen kunt krijgen en ontkoppelen met behulp van [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
