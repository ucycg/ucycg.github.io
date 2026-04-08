---
layout: default
---

# BACKUP

Ein Backup dient der Absicherung von sensiblen Daten und damit Informationen, um bei ungeplanten Verlusten oder Veränderung von Daten die Daten in Form eines Backups wiederherzustellen.

## Backup als Maßnahme zur Erhöhung der Verfügbarkeit

Ein Backup dient primär der **Datensicherheit** (Schutz vor Datenverlust) und NICHT der Verfügbarkeit. Es ermöglicht die **Wiederherstellung** nach einem Totalausfall (Disaster Recovery).

## Vollständiges Backup (VB)

- Speichert alle Daten auf einem separatem unabhängigem Laufwerk. Es wird also eine 1 zu 1 Kopie erschaffen.

![Vollbackup Diagram](/assets/images/hardware/backup/Vollbackup.svg)

**Vorteil**: Die Wiederherstellung mit dieser Art von Backup ist sehr simpel. Es ist ausreichend das VB auf den gewünschte Laufwerk zu übertragen. Dies ist außerdem schneller als mit den nachfolgenden Verfahren.

**Nachteil**: Es wird maximal viel Speicherplatz benötigt zur Erstellung eines VB. Außerdem ist die Erstellung eines VB zeitaufwändig.

## Differentielles Backup (DB)

- Diese Art des Backups wird im Zusammenspiel mit einem VB verwendet.
- Die Strategie hierbei ist, dass zum Zeitpunkt der Erstellung des DB alle Änderungen seit dem letzten VB gespeichert werden.

![Differentielles Backup Diagram](/assets/images/hardware/backup/DifferentiellesBackup.svg)

Vorteil: Dies spart Daten im Vergleich zu einem VB und kann auch schneller erzeugt werden.
Nachteil: Die Erstellung dauert länger als bei einem inkrementellen Backup (IB). Außerdem wird für ein DB mehr Speicherplatz benötigt als für ein IB. Schließlich braucht man zur Wiederherstellung immer das VB und das aktuelle DB.

## Inkrementelles Backup

- Diese Art des Backups wird im Zusammenspiel mit einem VB verwendet
- Die Strategie hierbei ist, dass zum Zeitpunkt der Erstellung des IB alle Änderungem seit dem letzten IB gespeichert werden.

![Inkrementelles Backup Diagram](/assets/images/hardware/backup/InkrementellesBackup.svg)

Vorteil: Lässt sich am schnellsten von allen hier vorgestellten Backups erzeugen. Außerdem benötigt es am wenigsten Speicherplatz.
Nachteil: Ist nur ein einziges IB seit dem letzten VB defekt, dann lassen sich verlorene Daten möglichweise nicht wiederherstellen.
