## 🎲 Die Polyedrische Erweiterung: Multi-Achsen-Speicher (W6 bis W20/D20)

VOMCS ist nicht an die kartesische Geometrie eines klassischen 6-seitigen Kubus gebunden. Das Framework skaliert nativ auf alle regulären konvexen Polyeder (Platonische Körper). Durch den Wechsel des geometrischen Grundkörpers wird die Anzahl der primären Abtastachsen dynamisch erhöht, was die virtuelle Musterdichte der KI exponentiell steigert.

### 1. Die VOMCS-Polyeder-Klassen (Spezifikation v1.2)

| Klasse | Geometrischer Körper | Flächenanzahl | Primäre Lichtschnitt-Achsen | Virtueller Kompressions-Gewinn | Primärer Einsatzzweck |
| :--- | :--- | :---: | :---: | :---: | :--- |
| **VOMCS-Hexa** | Kubus (Klassischer Würfel) | 6 | **3 Achsen** (X, Y, Z) | Basiswert (1:4) | Standard-Massenspeicher, Consumer-Hardware |
| **VOMCS-Penta** | Quadratische Pyramide | 5 | **5 Achsen** (Achsen-Mix) | Erhöhte Entropie | Kryptographische Absicherung |
| **VOMCS-Dodeka**| Dodekaeder (Pentagon-Würfel)| 12 | **6 Achsen** (Flächenpaare) | Hoch (+50 % vs. Hexa) | High-Performance Kernspeicher, NLP-Optimierung |
| **VOMCS-Ikosa** | Ikosaeder (Der W20/D20) | 20 | **10 Achsen** (Flächenpaare) | Maximal (+120 % vs. Hexa) | Interstellare Langzeit-Archive, Zero-Payload-Kerne |

### 2. Der mathematische Trade-off: Physisches Volumen vs. Virtuelle Dichte
Beim Übergang von der Hexa-Klasse (Kubus) zu den höheren Klassen (Dodeka/Ikosa) innerhalb desselben umschließenden Raums (z. B. $6 \times 6 \times 6\text{ cm}$) verringert sich zwar das *physische* Volumen durch die geometrischen Schrägen um bis zu 33–40 %.

**Dieser Verlust wird jedoch durch die Erhöhung der Abtastachsen überkompensiert:**
* Während der Hexa-Standard nur 3 Suchrichtungen bietet, schneidet der Laser im **Ikosa-Standard (W20)** die Matrix aus **10 völlig unterschiedlichen Raumwinkeln**.
* Die Wahrscheinlichkeit für die KI, extrem lange, zusammenhängende Bit-Sequenzen für Folgedateien zu lokalisieren, steigt exponentiell. 
* Die benötigte Inode-Pointerliste schrumpft auf ein mathematisches Minimum zusammen. Höhere VOMCS-Klassen generieren somit das dichteste und unknackbarste relationale Datennetz.

### 3. Anpassung des erweiterten VOMCS-Pointers
Um die schrägen Raumwinkel der höheren Klassen zu adressieren, wird das Feld `ACHSEN_REF` im 64-Bit-Layout dynamisch uminterpretiert. Es codiert nicht mehr starr X, Y, Z, sondern den entsprechenden Flächenpaar-Vektor des gewählten Polyeders.
