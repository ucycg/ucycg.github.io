---
layout: default
---

# Verkabelung

## Die drei Ebenen der Gebäudeverkabelung

| Level | Bildlich | Verbindet | Typisches Medium |
| :---: | :---: | :---: | :--- |
| **Primärverkabelung** | Campus | Verschiedene Gebäude eines Netzwerkes / KIT! | Single Mode Glasfaser |
| **Sekundärverkabelung** | Vertikale | Verschiedene Stockwerke eines Gebäudes | Multi Mode Glasfase -> strecken < 500m |
| **Tertiärverkablung** | Horizontale | Einzelne Clients in einer Etage | Kupfer Kabel -> Strecken < 100m |

## 2 Medien im Detail

### LWL

Methode zur optischen Signalübertragung. Extrem Hohe Übertragungsrate, hohe Bandbreite, geringe Verluste, keine Störanfälligkeit für EM Signale.

#### Single Mode LWL

Besonders verlustarm wird verwendet für Untersee Kabel oder kilometer lange leitungen, teurere aktive Betriebskomponenten mit Lasern(eine Wellenlänge), weniger flexibelere Kabel. Gewaltige, kilometerlange Reichweiten

#### Multi Mode LWL

Dickerer Kern (50 um)
Haben höhere Verluste als Single Mode und Signalverzerrung durch Modendispersion, dafür sind sie allerdings kostengünstiger, da für den Betrieb LEDs statt Laserdioden Technik genutzt werden kann.

### Kupfer Kabel Twisted Pair

Geringe Kosten, Adernpaare sind verdrillt, um elektromagnetische Störungen von außen und gegenseitiges Übersprechen (CrossTalk) zu verhinden. Außerdem ermöglicht Kupfer PoE für Geräte z.B. Access Points

Es gibt verschiedene Klassen dieser Kabel. Aktueller Standard im Büro Cat6a bzw Cat7 (10Gbit). Cat8 für kurze Strecken im Rechenzentrum.

## Die 2 Varianten einews Twisted Pair Kabels

Es gibt 2 verschiedene Arten wie ein RJ45 Ethernet Kabel  mit dem Stecker verkabelt wird. Sie werden für unterschiedliche Arten von Verbindungen eingesetzt.

### Straight Through (1:1 Patch Kabel)

Diese Variante bedeutet -> Tx zu Tx und Rx zu Rx. Diese Art wird für die Verbindung von unterschiedlichen Geräte genutzt -> z.B. PC mit Switch oder Switch mit Router verbinden

### Crossover

Diese Variante bedeutet wie der Name schon sagt, dass Tx mit Rx und Rx mit Tx verbunden und somit "Gekreuzt" werden. Dies wird dann im Gegensatz zu Straight Through für das direkte verbinden von gleichen Geräten genutzt z.B. für die Verbindung von 2 PCs untereinander ohne Geräte dazwischen. Oder um einen Switch an einen Switch anzuschließen.
