---
title: Licencia métrica
type: docs
weight: 80
url: /es/net/licencia-metrica/
description: PSD Photoshop C# Library permite a los desarrolladores aplicar una clave métrica que es un nuevo mecanismo de licencia y se utilizará junto con el método de licencia existente.
---

{{% alert color="primary" %}}

Aspose.PSD permite a los desarrolladores aplicar una clave métrica. Es un nuevo mecanismo de licencia. El nuevo mecanismo de licencia se utilizará junto con el método de licencia existente. Aquellos clientes que deseen ser facturados según el uso de las funciones de la API pueden utilizar la licencia métrica. Para obtener más detalles, consulte la sección de [Preguntas frecuentes sobre la licencia métrica](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Licencia métrica**
Aquí se muestran los pasos simples para usar la clase Métrica.

1. Crear una instancia de la clase Métrica.
1. Pasar claves públicas y privadas al método setMeteredKey.
1. Realizar el procesamiento (realizar la tarea).
1. Llamar al método getConsumptionQuantity de la clase Métrica.
1. Devolverá la cantidad/cantidad de solicitudes de la API que ha consumido hasta ahora.

A continuación se muestra el código de ejemplo que demuestra cómo establecer una clave pública y privada métrica.

{{< highlight java >}}

// Crear una instancia de la clase Métrica PSD

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Acceder a la propiedad setMeteredKey y pasar las claves públicas y privadas como parámetros

metered.SetMeteredKey("*****", "*****");



// Obtener la cantidad de datos métricos antes de llamar a la API

decimal cantidadAntes = Aspose.PSD.Metered.GetConsumptionQuantity();



// Mostrar información

Console.WriteLine("Cantidad consumida antes: " + cantidadAntes.ToString());

// Obtener la cantidad de datos métricos después de llamar a la API

decimal cantidadDespués = Aspose.PSD.Metered.GetConsumptionQuantity();



// Mostrar información

Console.WriteLine("Cantidad consumida después: " + cantidadDespués.ToString());

{{< /highlight >}}
