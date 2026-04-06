---
layout: default
---

# RAID

Mehrere physische Speicher werden zu einem logischen Laufwerk. Dieses hat dann eine **höhere Ausfallsicherheit** oder einen **größeren Datendurchsatz** als nur ein einzelner physischer Speicher.

## RAID0 (Striping)

![RAID0 Diagram](/assets/images/hardware/RAID0.svg)

RAID0 bietet **keine höhere Redundanz**. Damit ist es nur ein **"Array of Independent Discs"**. Wie der Name in der Überschrift schon vorgibt, werden die Daten in einzelne Streifen aufgeteilt und so gleichmäßig auf die verfügbaren Speichermedien aufgeteilt. Dies bietet dann **gesteigerte Datenraten** beim Zugriff.

## RAID1 (Mirroring)

![RAID1 Diagram](/assets/images/hardware/RAID1.svg)

Hier wird eine vollständige Kopie der gespeicherten Daten auf zusätzlichen physischen Speichern Deswegen auch der Name "Spiegelung". Dies gewährleistet **vollständige Redundanz** und kann den Ausfall eines physischen Speicher kompensieren. Dies ist allerdings **kein Ersatz für eine Datensicherung**. Die **Leseleistung  erhöht** sich durch RAID1 indem verschiedene Sektoren parallel verfügbar sind.

## RAID5 (Parity)

## RAID6 (Double Parity)
