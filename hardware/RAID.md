---
layout: default
---

# RAID

TO-DO: hier Übersichtstabelle einfügen!

Mehrere physische Speicher werden zu einem logischen Laufwerk. Dieses hat dann eine **höhere Ausfallsicherheit** oder einen **größeren Datendurchsatz** als nur ein einzelner physischer Speicher.

Die nachfolgende Tabelle bietet einen Überblick über die verschiedenen RAID Konfigurationen

| RAID level | Min. Disks | Fehlertoleranz | Nutzkapazität | Fokus |
| :---: | :---: | :---: | :--- | :--- |
| **0** | 2 | 0 | $100\%$ | Speed |
| **1** | 2 | 1 | $50\%$ | Sicherheit |
| **5** | 3 | 1 | $\frac{n-1}{n}$ | Wirschaftlichkeit |
| **6** | 4 | 2 | $\frac{n-2}{n}$ | Hochverfügbarkeit |
| **10** | 4 | 1 pro Mirror | $50\%$ | Performance + Sicherheit |

## RAID0 (Striping)

![RAID0 Diagram](/assets/images/hardware/RAID0.svg)

RAID0 bietet **keine höhere Redundanz**. Damit ist es nur ein **"Array of Independent Discs"**. Wie der Name in der Überschrift schon vorgibt, werden die Daten in einzelne Streifen aufgeteilt und so gleichmäßig auf die verfügbaren Speichermedien aufgeteilt. Dies bietet dann **gesteigerte Datenraten** beim Zugriff.

## RAID1 (Mirroring)

![RAID1 Diagram](/assets/images/hardware/RAID1.svg)

Hier wird eine vollständige Kopie der gespeicherten Daten auf zusätzlichen physischen Speichern Deswegen auch der Name "Spiegelung". Dies gewährleistet **vollständige Redundanz** und kann den Ausfall eines physischen Speicher kompensieren. Dies ist allerdings **kein Ersatz für eine Datensicherung**. Die **Leseleistung  erhöht** sich durch RAID1 indem verschiedene Sektoren parallel verfügbar sind.

## RAID5 (Parity)

![RAID5 Diagram](/assets/images/hardware/RAID5.svg)

RAID5 führt genauso wie RAID0 eine **Verteilung der Daten über verschiedene physische Speicher** durch allerdings ist zusätzlich der **vollständige Ausfall eines physischen Speichers kompensierbar**, da zusätzliche Partitätsbits für die verschiedenen Bereiche als Absicherung dienen. Insgesamt gibt es also eine **gesteigerte Datenrate beim Lesen** und eine **gute Redundanz** bei verhältnismäßig geringen zusätzlichen kosten. Damit ist RAID5 eine beliebte Variante

## RAID6 (Double Parity)

Dieses RAID Verfahren funktioniert genaus wie RAID5 allerdings wird die Anzahl der Partitätsbits pro Bereich verdoppelt auf 2. Mit diesem System kann folglich auch der Ausfall von 2 physischen Speichern kompensiert werden. Allerdings unter dem Einsatz eines weiteren zusätzlichen Speichers.

![RAID6 Diagram](/assets/images/hardware/RAID6.svg)

## RAID Kombinationen


TO-DO: Erklären wie man RAID Kombinationen aufbaut und wie sie dann exemplarisch aussehen!
