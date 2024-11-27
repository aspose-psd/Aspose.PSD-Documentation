---
title: Traitement des Données Brutes
type: docs
weight: 70
url: /fr/java/raw-data-processing/
---

## **Traitement des Données Brutes**
Pour améliorer les performances de l'API Aspose.PSD, nous avons introduit une méthode de traitement des données brutes avec la version 2.4.0. Le traitement des données brutes est désormais utilisé en interne et possède une API externe pour être utilisé en dehors de la bibliothèque afin d'améliorer les performances globales. Parfois, le traitement peut devenir un peu délicat et nécessiter quelques explications. Le traitement des données brutes est actuellement disponible uniquement pour le format BMP.

Pour aider les développeurs à obtenir les meilleures performances, l'API Aspose.PSD fournit un système de traitement des données brutes qui possède une API externe pour la personnalisation. Les développeurs appellent la famille de méthodes LoadRawData et SaveRawData pour utiliser le traitement des données brutes. Ces méthodes nécessitent également que le format de données brutes souhaité soit défini à l'aide de la classe RawDataSettings. La classe RawDataSettings permet aux développeurs de spécifier n'importe quel format de données brutes. Cependant, pour obtenir les meilleures performances, vous devez utiliser le format de données brutes dans lequel les données sont stockées. Les RawDataSettings définis dans la classe RasterImage aident à déterminer le format de données brutes de l'image. Lorsque vous transmettez une instance de RawDataSettings à la méthode LoadRawData, les données sont renvoyées telles quelles, sans aucune conversion appliquée, et peuvent améliorer les performances. En revanche, vous devez prendre en compte tous les formats de données brutes possibles, ce qui peut parfois être un peu compliqué.

Pour simplifier le processus de traitement, au prix d'une légère pénalité en termes de performances, vous pouvez spécifier les RawDataSettings souhaités en instanciant et en initialisant la classe avec les paramètres de données brutes désirés. Il y a des cas où il n'est pas possible de renvoyer les données brutes dans le format spécifié (par exemple, la conversion de l'espace colorimétrique CMJN en RVB n'est pas disponible dans la version 2.4.0). De plus, il pourrait y avoir des scénarios où le traitement des données brutes n'est pas du tout disponible pour un format d'image. Afin de déterminer si vous pouvez utiliser les méthodes familiales LoadRawData et SaveRawData, vous devez interroger la propriété IsRawDataAvailable.
### **Aperçu**
Pour le format de données des pixels RVB, il existe des formats de données brutes indexés (basés sur une palette) et RVB. Les formats de données brutes indexés contiennent des indexes d'entrée de palette dans la plage 0..(2^nombre de bits – 1). Les formats de données brutes indexés sont de 1, 2, 4 et 8 bits par pixel. Les autres formats sont basés sur RVB. Lors du chargement de données brutes, assurez-vous qu'il y a suffisamment d'octets disponibles pour charger les données, sinon une exception appropriée sera levée. Vous pouvez simplement estimer la taille du tableau d'octets en multipliant la taille de la ligne par le nombre de lignes nécessaires. La taille de la ligne peut varier et dépend du format de stockage des données brutes.

Pour obtenir les meilleures performances, utilisez toujours une taille de ligne de données brutes égale à la valeur de la propriété RasterImage.RawLineSize. Cependant, parfois vous devrez peut-être ajouter un rembourrage supplémentaire aux rangées de données brutes, ou le réduire, et dans ce cas, une taille de ligne différente peut être utilisée. Si un sous-ensemble d'un rectangle de délimitation d'image est requis, alors prenez en compte les décalages de bits qui peuvent se produire pour les formats de pixels RVB indexés. Par exemple, considérons une image avec des dimensions de 100x100 pixels et un format de données brutes de 1 bit par pixel. Vous souhaitez charger un rectangle de données brutes avec une dimension de (7,0) et (2,1), ou en d'autres termes, vous avez besoin de 2 pixels à partir de x=7 et y=0. Dans ce cas, vous devriez recevoir la disposition des données suivante:



![à faire:texte_alt_de_l'image](raw-data-processing_1.png)

Cela signifie que vous recevez 2 octets où le premier octet contient 7 pixels indésirables, puis 1 pixel souhaité, et le deuxième octet contient 1 pixel souhaité et ensuite 7 indésirables. Vous pouvez vous demander pourquoi nous n'avons pas effectué de décalage des données et mis ces 2 pixels dans un seul octet ? La réponse est simple : pour maintenir des performances élevées. Tous les traitements internes sont généralement effectués avec toutes les données à partir du premier pixel jusqu'au dernier pixel disponible. Il y a rarement des situations où un sous-ensemble de pixels est nécessaire. De plus, nous n'avons aucune idée de la manière dont ces pixels seront traités par la suite, donc le décalage ralentirait les performances et rendrait le code inutilement complexe. Estimez toujours le bon bit (pas besoin de déterminer le bon octet puisque les données viennent toujours avec le premier octet rempli) où les pixels demandés commenceront. Pour calculer le bon bit, une formule simple peut être utilisée : (rect.gauche * nombre de bits) % 8.
### **Conversion des Couleurs RVB Indexées**
Pour obtenir les meilleures performances possibles, utilisez toujours les mêmes paramètres de données brutes source et de destination, les formats de pixels et les tailles de ligne. Cependant, parfois vous devrez effectuer une conversion des données. Par exemple, vous pouvez charger une image RVB à 1 bit par pixel et l'enregistrer à 2 bits par pixel, ou charger une image RVB à 4 bits et réduire sa plage de couleurs à 2 bits par pixel. Dans les deux cas, une conversion des couleurs doit être appliquée. La conversion d'images RVB indexées peut parfois être délicate et ne peut être effectuée sans l'application de certains paramètres. Nous devons déterminer comment la plage de couleurs source est mappée sur l'espace colorimétrique cible. Pour accomplir cette tâche nous avons différents modes :

- Mappage de la palette (DitheringMethods.PaletteConversion)
- Mappage des données brutes (DitheringMethods.PaletteIgnore)
- Conversion personnalisée (DitheringMethods.CustomConverter)

Lorsque la conversion de palette est utilisée, l'espace colorimétrique source tente de correspondre le plus possible à l'espace colorimétrique cible. Par exemple, supposons que nous avons une image à 4 bits avec les couleurs suivantes :
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

L'image source ressemble à ceci :



![à faire:texte_alt_de_l'image](raw-data-processing_2.png)

Et nous convertissons l'image à 4 bits en une image à 1 bit avec les couleurs de la palette suivantes définies :

[0] RVB = 0, 0, 0
[1] RVB = 255, 255, 255

En mode de conversion de palette, le convertisseur lit la couleur source et détermine l'index cible en utilisant la méthode GetNearestColorIndex de la palette cible. La valeur de la propriété RasterImage.RawFallbackIndex est utilisée si la méthode GetNearestColorIndex de la palette renvoie un index hors de portée. Cela convertit les couleurs source en les couleurs cibles les plus proches en termes de valeurs d'intensité. L'image cible correspond le plus possible à l'image source. Vous pouvez voir le résultat suivant :



![à faire:texte_alt_de_l'image](raw-data-processing_3.png)

En mode de mappage des données brutes, un scénario différent est utilisé. Les palettes de couleurs source et cible sont simplement ignorées et les index source sont mappés sur les index de destination. Lorsqu'une valeur est trouvée qui ne peut pas être mappée dans la plage cible (en réduisant le nombre de bits), alors la valeur de propriété RasterImage.RawFallbackIndex est utilisée. La valeur est 0 par défaut et sera mappée sur la première couleur de la palette de destination. Si la valeur de cette propriété se situe en dehors de la plage de destination, une exception appropriée est levée. Cela conduit à des résultats moins prévisibles, comme le montre l'image suivante :



![à faire:texte_alt_de_l'image](raw-data-processing_4.png)

Le mode de conversion de palette est une solution plus correcte pour le problème de mappage des couleurs, mais il prend également un peu plus de temps pour s'achever, car des calculs doivent être effectués pour estimer le mappage correct des palettes. (Typiquement, il y a une très petite différence de performances entre les deux méthodes.) D'un autre côté, le mode de mappage des données brutes s'exécute un peu plus rapidement et peut être utilisé pour des conversions de couleurs plus brutes lorsque le mappage précis des couleurs n'est pas si important. Par exemple, il y a des cas où la palette de couleurs source est réduite et peut être convertie en comptages de bits inférieurs car les bits supplémentaires n'ont pas été utilisés de toute façon.

Pour utiliser l'une de ces approches, utilisez la propriété RawDitheringMethod de la classe RasterImage. Par défaut, elle est définie sur la méthode de conversion de palette pour obtenir les meilleurs résultats visuels. Vous pouvez modifier cette propriété avant toute conversion (lors de l'enregistrement de l'image dans un flux par exemple). Veuillez noter que les méthodes de mappage de la palette ignore et de conversion de la palette ne seront pas utilisées si vous avez chargé une image et réécrit une partie des données de pixels d'origine car les nouvelles données vont dans le cache et le cache stocke les données dans le format maximal disponible 32ARGB (à partir de la version 2.4.0, sujet à modification). Ce format est utilisé pour surmonter les problèmes de possibles plages de couleurs différentes pour les images chargées et enregistrées. De plus, les méthodes de mappage de la palette ignore et de conversion de la palette ne seront pas prises en compte lorsqu'une image est chargée en mode RVB et convertie en mode indexé ou vice versa.
### **Convertisseurs de Couleurs Personnalisés**
Parfois, il n'est pas suffisant d'utiliser l'approche standard pour la conversion des couleurs. Vous pouvez vouloir utiliser un algorithme personnalisé pour avoir une liberté totale lors de l'utilisation des routines de conversion des couleurs. Lorsque les formats de pixels des images source et cible sont tous les deux des formats RGB indexés, une interface plus simple, IIndexedColorConverter, peut être utilisée. Vous devez définir la propriété RasterImage.RawIndexedColorConverter sur une instance de l'interface IIndexedColorConverter et utiliser DitheringMethods.CustomConverter comme valeur de la propriété RawDitheringMethod. Lorsque cette combinaison est impliquée, alors toute conversion de couleurs indexées passe par cette instance spécifiée de IIndexedColorConverter. Le convertisseur de couleurs indexées personnalisé possède la méthode suivante définie :



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



La méthode FillIndexedtoIndexedMap est appelée lorsque la conversion est nécessaire d'une image RVB indexée à un format d'image RVB indexé (lorsque l'un des comptages de 1, 2, 4 ou 8 bits est converti en un autre). Le tableau de mappage a une longueur égale à tous les comptages d'entrées possibles du format source. Vous devez remplir ce tableau pour faire correspondre l'entrée de la palette de couleurs source à l'entrée de la palette de couleurs de destination. Assurez-vous que la valeur de l'index de destination se situe dans la plage de 0..(nombre de bits - 1), sinon une exception appropriée sera levée.

Si la nécessité est d'effectuer un scénario de conversion de couleurs plus personnalisé, alors la propriété RasterImage.RawCustomColorConverter doit être définie sur une instance de l'interface IColorConverter. La propriété RawCustomColorConverter remplace toujours la propriété RawIndexedColorConverter si les deux sont définies et un convertisseur de couleurs indexées ne sera pas utilisé dans ce cas. L'interface IColorConverter possède une seule méthode :



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}



La méthode Convert est appelée chaque fois qu'une conversion de couleurs est requise. La méthode reçoit les données brutes source dans le format source et possède un tampon de sortie pour recevoir le format couleur converti à la destination. Le tampon de destination doit être suffisant pour recevoir les données converties (si l'appel d'interface est effectué en interne par la bibliothèque Aspose.PSD) et doit contenir les données brutes converties lorsque la méthode retourne. La méthode Convert peut être appelée plusieurs fois jusqu'à ce que toutes les données sources soient couvertes.