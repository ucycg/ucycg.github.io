---
layout: default
---

# RAIDll

Mehrere physische Speicher werden zu einem logischen Laufwerk. Dieses hat dann eine **höhere Ausfallsicherheit** oder einen **größeren Datendurchsatz** als nur ein einzelner physischer Speicher.

Die nachfolgende Tabelle bietet einen Überblick über die verschiedenen RAID Konfigurationen

| RAID level | Min. Disks | Fehlertoleranz | Nutzkapazität | Fokus |
| :---: | :---: | :---: | :--- | :--- |
| **0** | 2 | 0 | 100% | Speed |
| **1** | 2 | 1 | 50% | Sicherheit |
| **5** | 3 | 1 | (n-1) / n | Wirschaftlichkeit |
| **6** | 4 | 2 | (n-2) / n | Hochverfügbarkeit |
| **10** | 4 | 1 pro Mirror | 50% | Performance + Sicherheit |
| **50** | 6 | 1 pro Mirror | (n-s)/n | Performance und Kapazität |  
| **06** | 8 | 2 | (n-2) / n | Theoretisches Maximum an Stripe Sicherheit |

Defintion: **s** steht hierbei für die **Anzahl von Sub-Arrays**

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

Die verschiedenen RAID Level lassen sich auch beliebig kombinieren. Die Schreibweise lautet dann jeweils RAIDXY, wobei die Hierarchie sich in Leserichtung aufbaut.

### Bsp RAID50

![RAID50 Diagram](/assets/images/hardware/RAID50.svg)

RAID50 bedeutet also, dass vollständige RAID5 Systeme zu RAID0 System zusammengeschaltet werden. Ein RAID50 System hat dann also mindestens 6 physikalische Speicher.

### Bsp RAID06

![RAID06 Diagram](/assets/images/hardware/RAID06.svg)

RAID06 bedeutet also, dass vollständige RAID0 Systeme zu einem RAID6 System zusammengeschaltet werden. Ein RAID06 System hat dann also mindestens 8 physikalische Speicher.
