---
title: Lista de los Recursos de Imágenes Globales PSD Soportados
type: docs
weight: 30
url: /es/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSD soporta la edición de bajo nivel de los Recursos de Imágenes.**
Lista de los Recursos de Imágenes completamente soportados que puede encontrar en Aspose.PSD .Net [Referencia de API](https://reference.aspose.com/psd/net)

Según la especificación del formato de Adobe® Photoshop®: Los recursos de imágenes utilizan varios números de ID estándar, como se muestra en los ID de recursos de imagen. No todos los formatos de archivo utilizan todos los ID. Algunas informaciones pueden estar almacenadas en otras secciones del archivo.

Para aquellos ID de recursos que se han añadido desde Photoshop 3.0, la entrada indica en qué versión fueron introducidos, por ejemplo (*Photoshop 6.0).*

ID del recurso de imagen.

|**ID**|**Descripción**|
| :- | :- |
|**Decimal**||
|1000|*(Obsoleto--Photoshop 2.0 solamente)* Número de canales, filas, columnas, profundidad y modo|
|1001|Registro de información de impresión del administrador de impresión de Macintosh|
|1002|Información del formato de página de Macintosh. Ya no leído por Photoshop. *(Obsoleto)*|
|1003|*(Obsoleto--Photoshop 2.0 solamente)* Tabla de colores indexados|
|1005|[Estructura de ResolutionInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource)|
|1006|Nombres de los canales alfa como una serie de cadenas de Pascal.|
|1007|*(Obsoleto) Ver la estructura de información de ID 1077 DisplayInfo*.|
|1008|El título como una cadena de Pascal.|
|1009|[Información de borde](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource). Contiene un número fijo (2 bytes reales,  2 bytes fracción) para el ancho del borde y 2 bytes para las unidades del borde (1 = pulgadas, 2 = cm, 3 = puntos, 4 = cicas, 5 = columnas).|
|1010|[Color de fondo. ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Marcas de impresión. Una serie de valores booleanos de un byte: etiquetas, marcas de corte, barras de color, marcas de registro, negativo, voltear, interpolar, título, marcas de impresión.|
|1012|Información de semitonos en escala de grises y multicanal|
|1013|[Información de semitonos de color](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Información de semitonos duotono|
|1015|Función de transferencia de escala de grises y multicanal|
|1016|[Funciones de transferencia de color](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Funciones de transferencia duotono|
|1018|Información de imagen duotono|
|1019|Dos bytes para los valores de negro y blanco efectivos para el rango de puntos|
|1020|*(Obsoleto)*|
|1021|Opciones EPS|
|1022|[Información de Máscara Rápida](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). ID de canal de Máscara Rápida; 1 byte booleano que indica si la máscara estaba inicialmente vacía.|
|1023|*(Obsoleto)*|
|1024|[Información de estado de capa](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Ruta de trabajo (no guardada). Formato de recurso de path.|
|1026|[Información de grupo de capas](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 bytes por capa que contienen un ID de grupo para los grupos de arrastre. Las capas en un grupo tienen el mismo ID de grupo.|
|1027|*(Obsoleto)*|
|1028|Registro IPTC-NAA. Contiene la información *File Info...*.|
|1029|Modo de imagen para archivos de formato raw|
|1030|Calidad JPEG. Privado.|
|1032|*(Photoshop 4.0) [Información de cuadrícula y guías](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresource)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Recurso de miniatura](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[para Photoshop 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* solamente|
|1034|*(Photoshop 4.0)* Marcador de copyright. Booleano que indica si la imagen tiene derechos de autor.|
|1035|*(Photoshop 4.0)* URL. Manejador de una cadena de texto con localizador uniforme de recursos*.*|
|1036|*(Photoshop 5.0)[Recurso de miniatura](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (sucede al recurso 1033).|
|1037|*(Photoshop 5.0) [Ángulo Global](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 bytes que contienen un entero entre 0 y 359, que es el ángulo global de iluminación para la capa de efectos. Si no está presente, se asume 30.|
|1038|*(Obsoleto) Ver el ID 1073 abajo. (Photoshop 5.0)* Recurso de selectores de color.|
|1039|*(Photoshop 5.0) [Perfil ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Los bytes crudos de un perfil de formato ICC (Consortium Internacional de Color).|
|1040|*(Photoshop 5.0) [Marca de agua](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [Perfil no etiquetado ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 byte que deshabilita cualquier manejo de perfil asumido al abrir el archivo. 1 = intencionalmente sin etiquetas.|
|1042|*(Photoshop 5.0)* Efectos visibles. Bandera global de 1 byte para mostrar/ocultar todas las capas de efectos. Solo presente cuando están ocultas.|
|1043|*(Photoshop 5.0)* Semitono de punto. 4 bytes para versión, 4 bytes para longitud y los datos de longitud variable.|
|1044|*(Photoshop 5.0)[IDs específicos del documento](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* semilla número. 4 bytes: valor base, a partir del cual se generarán los ID de capas (o un valor mayor si los ID existentes ya lo superan). Su propósito es evitar el caso en el que añadimos capas, aplanamos, guardamos, abrimos y luego agregamos más capas que terminan con los mismos ID que el primer conjunto.|
|1045|*(Photoshop 5.0) [Nombres Alfa Unicode](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Conteo de Tabla de Colores Indexados. 2 bytes para el número de colores en la tabla que están realmente definidos|
|1047|*(Photoshop 6.0)* [Índice de Transparencia](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Altitud Global.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Sectores.|
|1051|*(Photoshop 6.0)* URL de Flujo de Trabajo.|
|1052|*(Photoshop 6.0)* Ir a XPEP. 2 bytes para la versión principal, 2 bytes para la versión secundaria, 4 bytes para el conteo. Lo siguiente se repite para el conteo: 4 bytes para el tamaño del bloque, 4 bytes para la clave, si la clave = *'jtDd'* , entonces a continuación hay un Booleano para la bandera sucia; de lo contrario, es una entrada de 4 bytes para la fecha de modificación.|
|1053|*(Photoshop 6.0)* Identificadores Alfa.|
|1054|*(Photoshop 6.0)[Lista de URL](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* [Información de Versión](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource).|
|1058|*(Photoshop 7.0)* Datos EXIF 1.|
|1059|*(Photoshop 7.0)* Datos EXIF 3*.*|
|1060|*(Photoshop 7.0)* [Metadatos XMP](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Información de archivo como descripción XML.|
|1061|*(Photoshop 7.0)[Resumen de título](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 bytes: RSA Data Security, algoritmo de resumen de mensaje MD5|
|1062|*(Photoshop 7.0)[Escala de impresión](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = centrado, 1 = tamaño para ajustar, 2 = definido por el usuario). 4 bytes para la ubicación x (punto flotante). 4 bytes para la ubicación y (punto flotante). 4 bytes para la escala (punto flotante)|
|1064|*(Photoshop CS)* [Relación de Aspecto de Píxeles](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Capas de Composición.|
|1066|*(Photoshop CS)* Colores Duotonos Alternos. Este recurso no es leído o utilizado por Photoshop.|
|1067|*(Photoshop CS)* Colores de Mancha Alternos. Este recurso no es leído o utilizado por Photoshop.|
|1069|*(Photoshop CS2)* ID(s) de Selección de Capas. 2 bytes de conteo, lo siguiente se repite para cada conteo: 4 bytes de ID de capa|
|1070|*(Photoshop CS2)* Información de Tono de HDR|
|1071|*(Photoshop CS2)* Información de Impresión|
|1072|*(Photoshop CS2)* [ID de Grupos de Capas Habilitadas](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 byte para cada capa en el documento, repetido por la longitud del recurso. NOTA: Los grupos de capas tienen marcadores de inicio y fin|
|1073|*(Photoshop CS3)* Recurso de selectores de color. También ver ID 1038 para formato antiguo.|
|1074|*(Photoshop CS3)* Escala de Medición.|
|1075|*(Photoshop CS3)* Información de Línea de Tiempo.|
|1076|*(Photoshop CS3)* Divulgación de Hoja.|
|1077|*(Photoshop CS3) Estructura de DisplayInfo* para admitir colores de punto flotante. También ver ID 1007.|
|1078|*(Photoshop CS3)* Pieles de Cebolla.|
|1080|*(Photoshop CS4)* Información de Conteo.|
|1082|*(Photoshop CS5)* Información de Impresión.|
|1083|*(Photoshop CS5)* Estilo de Impresión. Las marcas de impresión, etiquetas, adornos, etc.|
|1084|*(Photoshop CS5)* NSPrintInfo de Macintosh. Información específica de OS variable para Macintosh.|
|1085|*(Photoshop CS5)* DEVMODE de Windows. Información específica de OS variable para Windows.|
|1086|*(Photoshop CS6)* Ruta de Guardado Automático.|
|1087|*(Photoshop CS6)* Formato de Guardado Automático. |
|1088|*(Photoshop CC)* Estado de Selección de Ruta.|
|2000-2997|Información de Ruta (rutas guardadas).|
|2999|Nombre de trayectoria de recorte.|
|3000|*(Photoshop CC)* Información de Origen de Ruta|
|4000-4999|Recurso(s) de Plug-In. Recursos añadidos por un complemento.|
|7000|Variables de Image Ready. Representación XML de la definición de variables|
|7001|Conjuntos de datos de Image Ready|
|7002|Estado seleccionado predeterminado de Image Ready|
|7003|Estado expandido al acercarse del rollover de Image Ready 7|
|7004|Estado expandido del rollover de Image Ready|
|7005|Ajustes de capa de guardado de Image Ready|
|7006|Versión de Image Ready|
|8000|*(Photoshop CS3)* Flujo de trabajo de Lightroom, si el documento está en medio de un flujo de trabajo de Lightroom.|
|10000|[Información de marcas de impresión](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource).|


Aspose.PSD soporta algunos de estos recursos. Si el Recurso no tiene su propia Clase, puede utilizar [UnknownResource ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource)de la Referencia de API de Aspose.PSD.

Los Recursos de Imágenes Globales PSD pueden ser utilizados para una gran cantidad de casos. Puede obtener Datos de Bajo Nivel específicos, que no puede obtener en Adobe Photoshop.

Además, siéntase libre de informar sobre Recursos de Imágenes que necesite. [El Foro de Aspose para PSD](https://forum.aspose.com/c/psd) puede ayudar.