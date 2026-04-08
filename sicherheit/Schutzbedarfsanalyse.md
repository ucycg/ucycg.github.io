---
layout: default
---

# Schutzbedarfsanalyse

## Unterschied Betriebssicherheit und Informationssicherheit

**Safety** - Betriebssicherheit -> Mein Sinnbild ist hier ein RAID-System

**Security** - Informationssicherheit -> Mein Sinnbild ist hier GIT als Tool Zur Versionskontrolle von Software

## Definition der Schutzziele

Dokumente zur Durchführung und Definition kommen vom BSI - Bundesamt für Sicherheit in der Informationstechnik

**Vertrauchlichkeit**: Schützen von Informationen vor unbefugtem Zugriff. Nur autorisierte Personen dürfen auf sensible Daten zugreifen.

![Not Authorized](/assets/images/sicherheit/Not_Authorized.png)

**BILD ANALOGIE**: Bei Github kann ich nur auf Repositories zugreifen, für die ich freigeschaltet bin -> sonst werden sie mir nicht angezeigt!

-> Mögliche Maßnahmen zur Umsetzung: Verschlüsselung, Zugriffskontrolle(chmod! wer hat welche Rechte?), Firewall

**Integrität**: Stellt sicher, dass Informationen unverändert und korrekt bleiben. Änderungen müssen nachvollziehbar sein. Nur befugte Personen dürfen Änderungen durchführen.

![Github_Branches](/assets/images/sicherheit/Github_Branches.png)

**BILD ANALOGIE 1** Es gibt bei Github den main-branch und feature-branches. Der Main Branch wird niemals direkt angefasst! Nur über einen PR und einen Merge kann man Änderungen vornehmen -> dadurch bleibt der main branch korrekt!

![Commits](/assets/images/sicherheit/Commits.png)

**BILD ANALOGIE 2** Außerdem gibt es Commits mit einem eindeutigen SHA

-> Mögliche Maßnahmen zur Umsetzung: Prüfsummen, Zugriffsrechte und regelmäßige Backups

**Verfügbarkeit**: Sorgt dafür, dass Informationen und Systeme zugänglich sind. Dies verhindert Systemausfälle und Datenverluste.

![Github_LocalRemote](/assets/images/sicherheit/GithubLocalRemote.svg)

**BILD ANALOGIE**: Remote und local bei Github -> immer regelmäßig Code änderungen committen und pushen, damit diese Informationen nicht verloren gehen.
-> Mögliche Maßnahmen zur Umsetzung: Redundante Systeme, Failover-Technologien und ein Disaster Recovery Plan

**GANZE ANALOGIE**:

ich lasse mir Rechte für ein neues Repo geben, dann schaue ich mir den Main Branch an und erstelle einen Feature Branch. Sobald ich Code geschrieben habe, mache ich einen Commit und pushen ihn an Remote!
