---
title: Traitement des Données Brutes
type: docs
weight: 50
url: /fr/traitement-des-donnees-brutes/
---

## **Traitement des Données Brutes**
Pour améliorer les performances de l'API Aspose.PSD, nous avons introduit une méthode de traitement des données brutes avec la version 2.4.0. Le traitement des données brutes est désormais utilisé en interne et dispose d'une API externe pour être utilisé en dehors de la bibliothèque afin d'améliorer les performances globales. Parfois, le traitement peut devenir un peu délicat et nécessiter des explications. Le traitement des données brutes est actuellement disponible uniquement pour le format BMP.

Pour aider les développeurs à obtenir les meilleures performances, l'API Aspose.PSD fournit un système de traitement des données brutes qui dispose d'une API externe pour la personnalisation. Les développeurs appellent la famille de méthodes [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) et [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) pour utiliser le traitement des données brutes. Ces méthodes nécessitent également que le format de données brutes désiré soit défini en utilisant la classe [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings). La classe RawDataSettings permet aux développeurs de spécifier n'importe quel format de données brutes. Cependant, pour obtenir les meilleures performances, vous devez utiliser le format de données brutes dans lequel les données sont stockées. Les RawDataSettings définis dans la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) aident à déterminer le format brut de [données de l'image](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat). Lorsque l'instance RawDataSettings est passée à la méthode LoadRawData, les données sont renvoyées telles quelles, sans aucune conversion appliquée, et peuvent améliorer les performances. D'un autre côté, vous devez prendre en compte tous les formats de données brutes possibles, ce qui peut parfois être un peu compliqué.

Pour simplifier le processus de manipulation, au détriment de quelques performances, vous pouvez spécifier les RawDataSettings désirées en instanciant et en initialisant la classe avec les paramètres de données brutes souhaités. Il arrive que ce ne soit pas possible de renvoyer les données brutes dans le format spécifié (par exemple, la conversion de l'espace colorimétrique CMJN en RVB n'est pas disponible dans la version 2.4.0). De plus, il peut y avoir des scénarios où le traitement des données brutes n'est pas du tout disponible pour un format d'image. Pour déterminer si vous pouvez utiliser les méthodes de la famille LoadRawData et SaveRawData, vous devez consulter la propriété [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable).
### **Perspicacité**
Pour le format de [données de pixels](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) RGB, il existe des formats de données brutes indexés (basés sur une palette) et basés sur RGB. Les formats de données brutes indexés contiennent les index des entrées de la palette dans la plage 0..(2^nombre de bits – 1). Les formats de données brutes indexés sont de 1, 2, 4 et 8 bits par pixel. Les autres sont des formats de données brutes basés sur RGB. Lors du chargement des données brutes, assurez-vous qu'il y a suffisamment d'octets disponibles pour charger les données, sinon une exception appropriée sera levée. Vous pouvez estimer simplement la taille du tableau d'octets en multipliant la taille de la ligne par le nombre de lignes requis. La taille de la ligne peut varier et dépend du format de stockage des données brutes.

Pour obtenir les meilleures performances, utilisez toujours une taille de ligne de données brutes égale à la valeur de la propriété [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize). Cependant, parfois, vous pouvez avoir besoin d'ajouter un remplissage supplémentaire aux lignes de données brutes, ou de le réduire, et dans ce cas, une taille de ligne différente peut être utilisée. Si un sous-ensemble d'un rectangle de délimitation d'image est requis, tenez compte des décalages de bit qui peuvent se produire pour les formats de pixels RGB indexés. Par exemple, considérons une image de dimensions 100x100 pixels avec un format de données brutes de 1 bit par pixel. Vous voulez charger un rectangle de données brutes avec l'emplacement (7,0) et les dimensions (2,1), ou en d'autres termes, vous avez besoin de 2 pixels à partir de x=7 et y=0. Dans ce cas, vous devriez recevoir la disposition des données suivante:



![todo:texte_alternatif_de_l'image](raw-data-processing_1.png)

Cela signifie que vous recevez 2 octets où le premier octet contient 7 pixels non désirés, puis 1 pixel désiré, et le deuxième octet contient 1 pixel désiré puis 7 non désirés. Vous pourriez vous demander pourquoi nous n'avons pas effectué de décalage de données et placé ces 2 pixels dans un seul octet ? La réponse est simple : pour maintenir des performances élevées. Tout traitement interne est généralement effectué avec l'ensemble des données à partir du premier pixel et se termine avec le dernier pixel disponible. Il est rare que seul un sous-ensemble de pixels soit nécessaire. De plus, nous ne savons pas comment ces pixels seront traités par la suite, donc un décalage ralentirait les performances et rendrait le code inutilement complexe. Estimez toujours le bon bit (pas besoin de déterminer le bon octet car les données arrivent toujours avec le premier octet rempli) à partir duquel les pixels demandés commenceront. Pour calculer le bon bit, une formule simple peut être utilisée : (rect.Left * nombre de bits) % 8.
### **Conversion de Couleurs Indexées RVB**
Pour obtenir les meilleures performances possibles, utilisez toujours les mêmes paramètres de données brutes source et de destination, les mêmes formats de pixels et les mêmes tailles de ligne. Cependant, parfois, vous pouvez avoir besoin d'effectuer une conversion de données. Par exemple, vous pouvez charger une image RVB de 1 bit par pixel et la sauvegarder avec 2 bits par pixel, ou charger une image RVB de 4 bits et réduire sa gamme de couleurs à 2 bits par pixel. Dans tous les cas, une conversion de couleurs doit être appliquée. Convertir des images RVB indexées peut parfois être délicat et ne peut être réalisé sans certains paramètres. Nous devons déterminer comment la plage de couleurs source est associée à l'espace colorimétrique cible. Pour accomplir cette tâche, nous avons différents [modes de conversion](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods):

- Mappage de palette (DitheringMethods.PaletteConversion)
- Mappage de données brutes (DitheringMethods.PaletteIgnore)
- Conversion personnalisée (DitheringMethods.CustomConverter)

Lorsque la conversion de la palette est utilisée, l'espace colorimétrique source tente de correspondre le plus possible à l'espace colorimétrique cible. Par exemple, admettons que nous ayons une image 4 bits avec les couleurs suivantes :
[0] RVB=0, 0, 0
[1] RVB=17, 17, 17
[2] RVB=34, 34, 34
[3] RVB=51, 51, 51
[4] RVB=68, 68, 68
[5] RVB=85, 85, 85
[6] RVB=102, 102, 102
[7] RVB=119, 119, 119
[8] RVB=136, 136, 136
[9] RVB=153, 153, 153
[10] RVB=170, 170, 170
[11] RVB=187, 187, 187
[12] RVB=204, 204, 204
[13] RVB=221, 221, 221
[14] RVB=238, 238, 238
[15] RVB=255, 255, 255

L'image source ressemble à ce qui suit:



![todo:texte_alternatif_de_l'image](raw-data-processing_2.png)

Et nous convertissons l'image 4 bits en une image 1 bit avec les couleurs de palette suivantes définies:

[0] RVB = 0, 0, 0
[1] RVB = 255, 255, 255

Dans le mode de conversion de palette, le convertisseur lit la couleur source et détermine l'index cible en utilisant la méthode [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) de la palette cible. La valeur de la propriété [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) est utilisée dans le cas où la méthode GetNearestColorIndex de la palette donne un index hors de portée. Cela convertit les couleurs source en les couleurs cibles les plus proches en termes de valeurs d'intensité. L'image cible correspond le plus possible à l'image source. Vous pouvez voir le résultat suivant:


![todo:texte_alternatif_de_l'image](raw-data-processing_3.png)

En mode de mappage de données brutes, un scénario différent est utilisé. Les palettes de couleurs source et cible sont simplement ignorées et les index source sont cartographiés sur les index de destination. Lorsqu'une valeur est trouvée qui ne peut pas être mappée dans la plage de destination (lors de la réduction du nombre de bits), alors la valeur de la propriété RasterImage.RawFallbackIndex est utilisée. La valeur est 0 par défaut et sera mappée sur la première couleur de la palette de destination. Si cette valeur de propriété se situe en dehors de la plage de destination, une exception appropriée est levée. Cela conduit à des résultats moins prévisibles, comme illustré dans l'image suivante:


![todo:texte_alternatif_de_l'image](raw-data-processing_4.png)

Le mode de conversion de palette est une solution plus correcte pour le problème de mappage des couleurs, mais il prend également un peu plus de temps à compléter car des calculs doivent être effectués pour estimer le mappage correct des palettes. (En général, il y a une très petite différence de performances entre les deux méthodes.) D'un autre côté, le mode de mappage brute s'exécute un peu plus rapidement et peut être utilisé pour une conversion de couleur plus brute lorsque le mappage exact des couleurs n'est pas si important. Par exemple, il y a des cas où la palette de couleurs source est tronquée et peut être convertie en toute sécurité en moins de bits car les bits supplémentaires n'ont pas été utilisés de toute façon.

Pour utiliser l'une de ces approches, utilisez la propriété RawDitheringMethod de la classe RasterImage. Par défaut, elle est définie sur la méthode de conversion de la palette pour obtenir les meilleurs résultats visuels. Vous pouvez modifier cette propriété avant toute conversion (par exemple lors de la sauvegarde de l'image dans un flux). Veuillez noter que les méthodes de diffusion de conversion de palette et d'ignorance de palette ne seront pas appliquées si vous avez chargé une image et réécrit certaines des données de pixels d'origine car les nouvelles données vont en cache et le cache stocke les données dans le format maximal disponible 32ARGB (à partir de 2.4.0, susceptible de changer). Ce format est utilisé pour surmonter les problèmes éventuels de plages de couleurs différentes pour les images chargées et enregistrées. De plus, les méthodes de diffusion de conversion de palette et d'ignorance de palette ne seront pas prises en compte lorsque une image est chargée en mode RGB et convertie en mode indexé ou vice-versa.
### **Convertisseurs de Couleurs Personnalisés**
Parfois, il n'est pas suffisant d'utiliser l'approche standard pour la conversion des couleurs. Vous pouvez souhaiter utiliser un algorithme personnalisé pour avoir une liberté totale lors de l'utilisation des routines de conversion de couleurs. Lorsque les formats de pixels des images source et cible sont tous deux des formats RGB indexés, une interface plus simple, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter), peut être utilisée. Vous devez définir la propriété [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) sur une instance de l'interface IIndexedColorConverter et utiliser le [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter pour la valeur de propriété RawDitheringMethod. Lorsque cette combinaison est impliquée, toute conversion de couleurs indexées passe par cette instance spécifiée d'IIndexedColorConverter. Le convertisseur de couleurs indexées personnalisé dispose de la méthode suivante définie:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



La méthode FillIndexedtoIndexedMap est appelée lorsque la conversion est nécessaire d'une image RGB indexée à un format d'image RGB indexée (lorsque l'un des 1, 2, 4 ou 8 bits est converti en l'autre). Le tableau de correspondance a une longueur égale au nombre total d'entrées de format source possibles. Vous devez remplir ce tableau pour faire correspondre l'entrée de la palette de couleurs source à l'entrée de la palette de couleurs de destination. Assurez-vous que la valeur de l'index de destination est dans la plage de 0..(nombre de bits - 1), sinon une exception appropriée est lancée.

Si le besoin est de réaliser un scénario de conversion de couleur plus personnalisé, la propriété [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) doit être définie sur une instance de l'interface [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter). La propriété RawCustomColorConverter remplace toujours la propriété RawIndexedColorConverter si les deux sont définies et un convertisseur de couleurs indexées ne sera pas utilisé dans un tel cas. L'IColorConverter dispose d'une seule méthode:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}


La méthode Convert est appelée chaque fois qu'une conversion de couleur est nécessaire. La méthode reçoit les données brutes source dans le format source et a un tampon de sortie pour recevoir le format de couleur converti à la destination. Le tampon de destination doit être suffisant pour recevoir les données converties (si l'appel à l'interface est fait en interne par la bibliothèque Aspose.PSD) et devrait contenir les données brutes converties à la fin de la méthode. La méthode Convert peut être appelée plusieurs fois jusqu'à ce que toutes les données source soient couvertes.