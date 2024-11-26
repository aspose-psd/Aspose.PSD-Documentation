---
title: Problemas Conhecidos
type: docs
weight: 40
url: /pt/net/known-issues/
---

## **.NET Compact Framework**
- Observou-se que em algumas versões específicas do Windows, como Windows Mobile 5.0-6.0, as assemblies do compact framework assinadas com certificado (ou certificados de assinatura dupla) não funcionam conforme o esperado e não conseguem ser carregadas corretamente (uma TypeLoadException é lançada). Para superar o problema, o usuário precisa remover qualquer certificado e, em seguida, usar a assembly atualizada. Por favor, note que você faz isso por sua própria conta e risco e não garantimos um funcionamento válido devido a essa mudança na assembly. Também não enviamos assemblies sem assinatura, já que isso representa uma ameaça de segurança potencial. Em vez disso, os clientes devem evitar usar sistemas operacionais antigos, se possível, e/ou atualizar o sistema operacional para edições mais recentes ou service packs que resolvam o problema de assinatura de certificado.
