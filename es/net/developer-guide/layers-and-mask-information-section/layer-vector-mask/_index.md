---
title: Máscara Vectorial de Capa
type: docs
weight: 10
url: /es/net/layer-vector-mask/
---

## **Resumen de la Máscara Vectorial de Capa**
Una máscara vectorial es una ruta independiente de la resolución que recorta el contenido de la capa. Las máscaras vectoriales suelen ser más precisas que las creadas con herramientas basadas en píxeles. Puede crear máscaras vectoriales con la pluma o las herramientas de formas.

Aspose.PSD admite la representación y aplicación de máscaras vectoriales. Puede editar máscaras vectoriales mediante la edición de Trayectorias Vectoriales.

## **Trayectoria vectorial en Aspose.PSD**
El acceso a las trayectorias vectoriales en Aspose.PSD se proporciona a través de los recursos [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) y [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) que son clases secundarias de [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:texto_alternativo_de_imagen](layer-vector-mask_0.png)

## **¿Cómo editar una trayectoria vectorial?**
### **Estructura de trayectoria vectorial**
La estructura base para manipular trayectorias es [VectorPathRecord](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord). Pero para su comodidad, se sugiere la siguiente solución.

Para la edición fácil de trayectorias vectoriales, debe usar la clase [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), que contiene métodos para la edición cómoda de los datos vectoriales en los recursos derivados de VectorPathDataResource

Comience creando un objeto del tipo VectorPath.

Para mayor comodidad, puede utilizar el método estático [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), este método encontrará un recurso vectorial en la capa de entrada y creará un objeto VectorPath basado en él.

Después de todas las ediciones, puede aplicar el objeto VectorPath con cambios nuevamente a la capa utilizando el método estático [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

El tipo VectorPath contiene una lista de elementos de [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) y describe una imagen vectorial completa que puede constar de una o más formas.

![todo:texto_alternativo_de_imagen](layer-vector-mask_1.png)


Cada PathShape es una figura vectorial que consta de un conjunto separado de puntos de curva Bezier.

Los puntos de curva Bezier son objetos del tipo [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) que son esencialmente los puntos a partir de los cuales se construye la figura.

![todo:texto_alternativo_de_imagen](layer-vector-mask_2.png)

El siguiente ejemplo de código muestra cómo acceder a una figura y a puntos.

{{< gist "aspose-com-gists" "8a4dround-pointts as elements of a regularranshantt with the same values,s." >}}

## **Propiedades de PathShape**
La edición de PathShape no se limita a la edición de nodos, este tipo también tiene otras propiedades.
### **Operaciones de Trayectoria (Operaciones booleanas)**
La propiedad [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) es una llamada operación booleana, cambiar el valor de la cual define cómo se mezclan múltiples formas.

Existen los siguientes valores posibles:

- 0 = ExcludeOverlappingShapes (operación XOR).
- 1 = CombineShapes (operación OR).
- 2 = SubtractFrontShape (operación NOT).
- 3 = IntersectShapeAreas (operación AND).

![todo:texto_alternativo_de_imagen](layer-vector-mask_4.png)

### **Propiedad IsClosed**
Además, utilizando la propiedad PathShape.IsClosed, podemos determinar si el primer y el último punto de curva de una forma están conectados.

|**Forma Cerrada**|**Forma Abierta**|
| :- | :- |
|![todo:texto_alternativo_de_imagen](layer-vector-mask_5.png)|![todo:texto_alternativo_de_imagen](layer-vector-mask_6.png)|

### **Propiedad FillColor**
Ninguna figura puede tener su propio color, por lo que puede cambiar el color de toda la trayectoria vectorial con la propiedad VectorPath.FillColor.

Puede manipular los puntos de la forma como elementos de una Lista regular utilizando la propiedad PathShape.Points, por ejemplo, puede agregar puntos de forma:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}

## **Aquí encontrará el código fuente de VectorDataProvider y clases relacionadas:**
{{< gist "aspose-com-gists" "8a4dround-pointts as elements of a regularranshantt with the same values,s." >}}
