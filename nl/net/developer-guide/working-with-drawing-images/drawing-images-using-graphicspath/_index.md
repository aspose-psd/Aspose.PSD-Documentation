---
title: Tekenen van afbeeldingen met behulp van GraphicsPath
type: docs
weight: 30
url: /nl/net/tekenen-van-afbeeldingen-met-graphicspath/
---

## **Tekenen van afbeeldingen met behulp van GraphicsPath**
De [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) klasse is verantwoordelijk voor het maken en onderhouden van een grafisch pad. De GraphicsPath heeft geen referentie naar een afbeelding en verandert de afbeelding zelf niet, in plaats daarvan kan het worden beschouwd als een object dat metagegevens bevat die de paden beschrijven die de Graphics-klasse kan tekenen. De GraphicsPath-klasse gebruikt figuren; elke figuur bestaat uit een reeks verbonden lijnen en bochten of een geometrische vorm. Elke vorm kan worden opgesplitst in vormsegmenten. U kunt verschillende figuren of vormen toevoegen, verwijderen en wijzigen in een GraphicsPath-object. Wanneer de GraphicsPath volledig is beschreven, gebruikt u de overeenkomstige methoden van de Graphics-klasse (DrawPath en Fill Paths) om over de paden te tekenen of de paden te vullen. De Graphics-klasse neemt elk vormsegment en tekent het om de eindafbeelding te produceren.
### **Tekenen met behulp van GraphicsPath-klasse**
Hieronder staat een voorbeeld dat het gebruik van de [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) klasse demonstreert. De voorbeeldbroncode is opgesplitst in verschillende delen om het eenvoudig en gemakkelijk te volgen te houden. Stap voor stap laten de voorbeelden zien hoe je:

- Een afbeelding maken.
- Initialiseren van een Graphics object.
- Het oppervlak wissen.
- Een instantie van [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) maken.
- Een figuur maken.
- Vormen toevoegen aan de figuur.
- Een array van figuren maken.
- Pad tekenen.
- Pad vullen.


### **Afbeeldingen tekenen met GraphicsPath: Programmeervoorbeelden**
#### **GraphicsPath: Maak een Afbeelding**
Begin met het maken van een afbeelding met behulp van een van de methoden die worden beschreven in Bestanden maken.
#### **GraphicsPath: Initialiseren van een Graphics Object**
Maak en initialiseer een Graphics object door het Image object door te geven aan de constructor.
#### **GraphicsPath: Wis het Oppervlak**
Wis het grafische oppervlak door de Clear-methode van de Graphics-klasse aan te roepen en een Kleur door te geven als parameter. Deze methode vult het grafische oppervlak met de opgegeven kleur.
#### **GraphicsPath: Maak een Instantie van de GraphicsPath**
Maak een instantie van GraphicsPath met GraphicsPath standaard ingesteld op Alternate. Deze modus bepaalt hoe het interieur van een gesloten figuur moet worden gevuld. De andere mogelijke waarde van GraphicsPath is Winding.
#### **GraphicsPath: Maak een Figuur**
Maak een instantie van de Figure-klasse. Zoals eerder besproken kan een Figuur Shapes bevatten en shapes bevinden zich in de Aspose.PSD.Shapes namespace.
#### **GraphicsPath: Voeg Vormen toe aan de Figuur**
De Add Shapes-methode die wordt blootgesteld door de Figure-klasse stelt je in staat vormen toe te voegen aan de figuur. In de onderstaande codevoorbeelden worden verschillende vormen toegevoegd aan een Figure-object.
#### **GraphicsPath: Voeg Figuren toe aan een Array**
Meerdere figuren kunnen worden toegevoegd aan een GraphicsPath-object met behulp van de AddFigures-methode die wordt blootgesteld door de GraphicsPath-klasse. Deze methode accepteert een array van figuren als parameter.
#### **GraphicsPath: Teken de Pad**
Teken de GraphicsPath met behulp van de DrawPath-methode die wordt blootgesteld door de Graphics-klasse. De methode accepteert twee parameters. Het eerste parameter is een object van de Pen-klasse, die de kleur, breedte en stijl van het pad bepaalt. Het tweede parameter is het object van de GraphicsPath-klasse, dat het pad zelf vertegenwoordigt.
#### **GraphicsPath: Vul Paden**

Je kunt een pad vullen door een GraphicsPath-object door te geven aan de Fill Paths-methode die wordt blootgesteld door de Graphics-klasse. De Fill Paths-methode vult het pad volgens de huidige vulmodus (alternate of winding) die is ingesteld voor het pad. Als het pad open figuren heeft, wordt het pad gevuld alsof die figuren gesloten waren.

De Fill Paths-methode accepteert twee parameters. Het eerste parameter is een object van een borstelklasse uit de Aspose.PSD.Brushes-namespace. Het tweede parameter is het pad zelf. Voor dit voorbeeld gebruik je de HatchBrush, dat is een rechthoekige borstel met een hatch-stijl, een voorgrondkleur en een achtergrondkleur. Voordat je het HatchBrush-object doorgeeft aan de Fill Paths-methode, stel je de eigenschappen ervan in.
### **GraphicsPath: Volledige Bron**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Alle klassen die IDisposable implementeren worden geïnstantieerd in een Using-statement om ervoor te zorgen dat ze correct worden weggegooid.
