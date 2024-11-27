---
title: Bekannte Probleme
type: docs
weight: 40
url: /de/net/known-issues/
---

## **.NET Compact Framework**
- Es wird beobachtet, dass auf bestimmten Windows-Versionen wie Windows Mobile 5.0-6.0 die Compact Framework-Assemblys, die mit einem Zertifikat signiert sind (oder doppelt signierte Zertifikate), nicht wie erwartet funktionieren und nicht korrekt geladen werden können (eine TypeLoadException wird ausgelöst). Um das Problem zu überwinden, muss der Benutzer alle Zertifikate entfernen und dann die aktualisierte Assembly verwenden. Bitte beachten Sie, dass dies auf eigenes Risiko geschieht und wir keine fehlerfreie Funktionsweise aufgrund einer solchen Änderung der Assembly garantieren. Auch versenden wir keine Assemblys ohne Signatur, da dies eine potenzielle Sicherheitsbedrohung darstellt. Stattdessen sollten Kunden, wenn möglich, den Gebrauch solcher veralteter Betriebssysteme vermeiden und/oder das Betriebssystem auf neuere Editionen oder Service Packs aktualisieren, die das Problem der Zertifikatssignierung beheben.
