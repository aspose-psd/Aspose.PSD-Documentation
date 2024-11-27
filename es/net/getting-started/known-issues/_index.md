---
title: Problemas Conocidos
type: docs
weight: 40
url: /es/net/known-issues/
---

## **.NET Compact Framework**
- Se ha observado que en algunas versiones específicas de Windows, como Windows Mobile 5.0-6.0, las asambleas del framework compacto firmadas con certificado (o certificados doblemente firmados) no funcionan como se esperaba y no pueden cargarse correctamente (se produce una TypeLoadException). Para superar el problema, el usuario debe eliminar cualquier certificado y luego utilizar la asamblea actualizada. Tenga en cuenta que realiza esta acción bajo su propio riesgo y no garantizamos un funcionamiento válido debido a dicho cambio de asamblea. Tampoco distribuimos asambleas sin firma, ya que esto es una amenaza de seguridad potencial. En su lugar, los clientes deberían evitar el uso de esos antiguos sistemas operativos, si es posible, y/o actualizar el sistema operativo a ediciones más nuevas o paquetes de servicio que resuelvan el problema de firma de certificados.
