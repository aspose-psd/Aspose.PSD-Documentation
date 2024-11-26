---
title: Gebruik van Graphics API om Lagen in PSD-bestanden te bewerken
weight: 100
type: docs
description: Voorbeeld van het gebruik van de Graphics API in Aspose.PSD voor Java
keywords: [laag bijwerken, cirkel tekenen, ellips tekenen, gevulde cirkel tekenen, graphics, psd api, java, voorbeeldcode]
url: nl/java/graphics-api/
---

## **Overzicht**
Om te beginnen, laadt het PSD-bestand met behulp van de Image.load() methode of maak een Psd Image vanaf nul. Gebruik de inputFile variabele om het pad naar uw PSD-bestand aan te geven, en specificeer eventuele laadopties met loadOpt, indien nodig.

Vervolgens, benader de eerste laag van het PSD-beeld met behulp van de psdImage.getLayers()[0] syntaxis om een verwijzing naar het laagobject te verkrijgen voor manipulatie.

Om de laag te bewerken, maak een Graphics object door de laag als parameter door te geven. Dit object biedt verschillende methoden voor het tekenen van vormen en het toepassen van penselen.

Een Pen object wordt gebruikt om de kleur en dikte van de omtrek van vormen te definiëren. Op dezelfde manier worden penselen zoals LinearGradientBrush gebruikt om vulkleuren te definiëren.

Teken vormen op de laag met behulp van methoden zoals graphics.drawEllipse() om vormen te omlijnen en graphics.fillEllipse() om ze te vullen.

Nadat u de gewenste wijzigingen aan de laag hebt aangebracht, slaat u het gewijzigde PSD-beeld op met psdImage.save().

Daarnaast kunt u het gewijzigde beeld opslaan in andere formaten zoals PNG door gebruik te maken van de juiste opties.

Dat is alles! U heeft met succes de Graphics API van Aspose.PSD voor Java gebruikt om lagen in een PSD-bestand te bewerken. Verken meer functies en mogelijkheden van de Aspose.PSD-bibliotheek om uw mogelijkheden voor het bewerken van afbeeldingen uit te breiden.

Gelieve het volledige voorbeeld te controleren.

## **Voorbeeld**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
