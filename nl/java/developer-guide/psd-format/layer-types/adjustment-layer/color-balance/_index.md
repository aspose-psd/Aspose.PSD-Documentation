---
title: Kleurbalans Aanpassingslaag
type: docs
weight: 30
url: /nl/java/layer-types/adjustment-layer/color-balance/
---

# Werken met Photoshop Kleurbalans aanpassingslaag in Java

In dit artikel gaan we de **kleurbalans van de afbeelding aanpassen** in PSD-bestandsindeling in Java. We zullen een speciale bibliotheek genaamd Aspose.PSD voor Java gebruiken, dat een gereedschapskist is voor het manipuleren van Photoshop documenten.

Aangezien de bibliotheek werkt met de PSD-bestandsindeling, bevat het bijna [alle functies](https://docs.aspose.com/psd/java/features/) die beschikbaar zijn in de Photoshop-editor en de **Kleurbalans aanpassingslaag**, die absoluut geschikt is voor deze taak, is geen uitzondering.

De Kleurbalans aanpassingslaag maakt het mogelijk om het evenwicht tussen primaire (RGB) en subtractieve (CMY) kleuren voor schaduwen, middentonen en hooglichten op een eenvoudige en snelle manier te veranderen.

## Kleurbalans Aanpassen

Zoals eerder vermeld, is de Kleurbalans aanpassingslaag in Aspose.PSD voor Java precies wat het is **een balans tussen primaire en subtractieve kleuren**. Dit betekent dat er drie schalen zijn voor elk kleurpaar (cyaan/rood, magenta/groen, geel/blauw). De intensiteit van een bepaalde kleur in het paar zal toenemen als de waarde daarnaartoe beweegt en vice versa. Bovendien zijn deze drie paren inherent aan elk gebied van het toonbereik (schaduwen, middentonen en hooglichten), wat de flexibiliteit van dit soort aanpassing verhoogt.

Laten we deze kennis nu in de praktijk toepassen. Als voorbeeld kiezen we een roodachtige foto van het gezicht van een vrouw (b). Het gezicht is zo roodachtig en we gaan dat corrigeren door **een Kleurbalans aanpassingslaag toe te voegen** om rood te verminderen en in feite cyaan te verhogen (a) om het gezicht er natuurlijker uit te laten zien (c). Nogmaals, er is veel werk te verrichten met deze afbeelding, maar in dit artikel is dit alles wat we zullen doen.

![Voorbeeld van Kleurbalans aanpassingslaag](color-balance-adjustment-layer-example-figure-1.png) De API van de Kleurbalans aanpassingslaag heeft een vlak ontwerp. Daarom is de [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) klasse alles wat je nodig hebt. Allereerst, behoud de helderheid omdat deze standaard is uitgeschakeld. Voeg vervolgens wat groen toe en wat meer geel voor schaduwen met behulp van overeenkomstige methoden (waarvan de namen bestaan uit de naam van het specifieke toonbereik en de kleurnamen in het kleurpaar), voeg dan meer cyaan toe en een beetje blauw voor middentonen, en voeg tot slot meer cyaan toe naast een beetje magenta en blauw:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Nu hebben we de foto die we wilden! Zo eenvoudig is het, toch?

Let op dat _de waarde van elk kleurpaar moet liggen tussen -100 en 100_ dat wil zeggen negatieve waarden voor subtractieve kleuren en positieve voor primaire kleuren respectievelijk, net zoals in de Photoshop-editor.

Raadpleeg onze API-referentie om meer technische details te weten te komen over de [Kleurbalans aanpassingslaag](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Conclusie

In dit artikel hebben we besproken hoe je de Kleurbalans van de afbeelding programmatisch kunt aanpassen in Java met behulp van de bibliotheek Aspose.PSD voor Java. De bibliotheek bevat een volledig uitgeruste API om te werken met Kleurbalans aanpassingslagen in Photoshop-documenten.
