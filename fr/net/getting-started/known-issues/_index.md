---
title: Problèmes Connus
type: docs
weight: 40
url: /fr/net/known-issues/
---

## **.NET Compact Framework**
- Il a été observé que sur certaines versions spécifiques de Windows telles que Windows Mobile 5.0-6.0, les assemblies du compact framework signés avec un certificat (ou des certificats signés en double) ne fonctionnent pas comme prévu et ne parviennent pas à se charger correctement (une TypeLoadException est lancée). Pour surmonter le problème, l'utilisateur doit supprimer tout certificat, puis utiliser l'assembly mis à jour. Veuillez noter que vous le faites à vos propres risques et nous ne garantissons pas un fonctionnement correct en raison de ce changement d'assembly. Nous ne livrons pas non plus d'assemblies sans signature, car cela représente une menace sécuritaire potentielle. Au lieu de cela, les clients devraient éviter d'utiliser de tels anciens systèmes d'exploitation, si possible, et/ou mettre à niveau le système d'exploitation vers des éditions ou des packs de services plus récents qui résolvent le problème de signature de certificats.

