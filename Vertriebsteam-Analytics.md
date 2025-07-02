# Bearlocal Vertriebsteam Analytics Dashboard fur Juni 2025 - Mathematische Analyse
Link : https://bearlocal-user-analytics-ftz8kjf7e-yuvraj-shekhars-projects.vercel.app/

## Inhaltsverzeichnis
1. [Alle Anrufe Analytik](#abschnitt-1-alle-anrufe-analytik)
2. [Anrufe über 1 Minute Analytik](#abschnitt-2-anrufe-über-1-minute-analytik)
3. [Konversionsraten-Erfolg Analytik](#abschnitt-3-konversionsraten-erfolg-analytik)

---

## Abschnitt 1: Alle Anrufe Analytik

### 1.1 Berechnung des Rentabilitätswerts

Der Rentabilitätswert ist eine gewichtete zusammengesetzte Metrik, die drei Schlüsselleistungsindikatoren kombiniert:

**Formel:**
```
Rentabilitätswert = (0,40 × Volumenwert) + (0,30 × Effizienzwert) + (0,30 × Qualitätswert)
```

#### Komponentenberechnungen:

**Volumenwert:**
- Misst die Gesamtleistung der verbundenen ausgehenden Anrufe
- Formel: `(Verbundene Anrufe des Mitarbeiters / Maximale verbundene Anrufe) × 100`
- Beispiel: Janis hat 790 verbundene Anrufe (Maximum), also Volumenwert = 100%
- Joshua hat 572 verbundene Anrufe, also Volumenwert = (572/790) × 100 = 72,4%

**Effizienzwert:**
- Misst Anrufe pro Arbeitsstunde
- Formel: `(Anrufe pro Stunde des Mitarbeiters / Maximale Anrufe pro Stunde) × 100`
- Anrufe pro Stunde = Verbundene ausgehende Anrufe / Gesamtarbeitsstunden
- Beispiel: Joshua hat 89,4 Anrufe/Stunde (Maximum), also Effizienzwert = 100%
- Janis hat 45,1 Anrufe/Stunde, also Effizienzwert = (45,1/89,4) × 100 = 50,4%

**Qualitätswert:**
- Misst die Verbindungserfolgsrate
- Formel: `(Verbindungsrate des Mitarbeiters / Maximale Verbindungsrate) × 100`
- Verbindungsrate = (Verbundene Anrufe / Gesamtversuche) × 100
- Beispiel: Robin hat 81,3% Verbindungsrate (Maximum), also Qualitätswert = 100%
- Janis hat 76,6% Verbindungsrate, also Qualitätswert = (76,6/81,3) × 100 = 94,2%

#### Endgültige Rentabilitätswerte:
- **Joshua: 86,2** = (0,40 × 72,4) + (0,30 × 100) + (0,30 × 90,8)
- **Janis: 83,4** = (0,40 × 100) + (0,30 × 50,4) + (0,30 × 94,2)
- **Robin: 82,2** = (0,40 × 85,4) + (0,30 × 60,1) + (0,30 × 100)
- **Iris: 59,6** = (0,40 × 53,9) + (0,30 × 36,4) + (0,30 × 90,3)

### 1.2 Erklärung der Graphenanalyse

#### 1.2.1 Vergleich verbundener ausgehender Anrufe (Balkendiagramm)
- **Zweck:** Visueller Vergleich der absoluten Anrufvolumen
- **Daten:** Rohe Anzahl verbundener Anrufe pro Mitarbeiter
- **Erkenntnis:** Janis führt im Volumen (790), berücksichtigt aber nicht die Effizienz

#### 1.2.2 Verbindungsratenanalyse (Balkendiagramm)
- **Berechnung:** (Verbundene Anrufe / Gesamtversuche) × 100
- **Ergebnisse:**
  - Robin: 81,3% (675/830)
  - Janis: 76,6% (790/1.032)
  - Joshua: 73,8% (572/775)
  - Iris: 73,4% (426/580)
- **Erkenntnis:** Robin hat die höchste Qualität trotz nicht höchstem Volumen

#### 1.2.3 Wöchentliche Leistungstrends (Liniendiagramm)
- **Zweck:** Verfolgung der Leistungskonsistenz über die Zeit
- **Berechnung:** Wöchentlich verbundene Anrufe für jeden Mitarbeiter
- **Haupterkenntnisse:**
  - Woche 4 zeigt signifikanten Rückgang (Juni Teilwoche)
  - Janis hält das konsistenteste hohe Volumen
  - Joshua zeigt abnehmenden Trend

#### 1.2.4 Rentabilitätswert-Komponenten (Gestapeltes Balkendiagramm)
- **Visualisierung:** Zeigt den Beitrag jeder Komponente zum Gesamtwert
- **Maximal möglich:** 100 Punkte (40 + 30 + 30)
- **Erkenntnis:** Joshua maximiert Effizienz trotz geringerem Volumen

#### 1.2.5 Anrufvolumenverteilung (Ringdiagramm)
- **Gesamtanrufe:** 2.463 verbundene Anrufe
- **Verteilung:**
  - Janis: 32,1% (790/2.463)
  - Robin: 27,4% (675/2.463)
  - Joshua: 23,2% (572/2.463)
  - Iris: 17,3% (426/2.463)

#### 1.2.6 Effizienzmetriken (Netzdiagramm)
- **Dimensionen:** 
  - Anrufe/Stunde (normalisiert auf Joshuas 89,4)
  - Verbindungsrate (normalisiert auf Robins 81,3%)
  - Gesamtvolumen (normalisiert auf Janis' 790)
  - Effizienz (zusammengesetzte Metrik)
- **Zweck:** Mehrdimensionale Leistungsvisualisierung

### 1.3 Berechnung von Schlüsselmetriken

**Auslastungsrate:**
- Formel: `Gesamte Anrufstunden / (160 Stunden × gearbeitete Wochen)`
- Nimmt 40-Stunden-Woche an
- Beispiel: Janis arbeitete 17,5 Stunden an Anrufen von ~160 möglichen = 10,9%

**Fehlgeschlagene Anrufe:**
- Berechnung: Gesamtversuche - Verbundene Anrufe
- Prozentsatz: (Fehlgeschlagene Anrufe / Gesamtversuche) × 100

---

## Abschnitt 2: Anrufe über 1 Minute Analytik

### 2.1 Modifizierter Rentabilitätswert für lange Anrufe

Die Berechnungsmethodik bleibt gleich, konzentriert sich aber nur auf Anrufe, die länger als 1 Minute dauern:

**Formel:**
```
Rentabilität langer Anrufe = (0,40 × Langer Volumenwert) + (0,30 × Langer Effizienzwert) + (0,30 × Langer Qualitätswert)
```

#### Komponentenberechnungen:

**Langer Volumenwert:**
- Basiert nur auf Anrufen >1 Minute
- Maximum: Janis mit 592 langen Anrufen
- Beispiel: Robin = (540/592) × 100 = 91,2%

**Langer Effizienzwert:**
- Lange Anrufe pro Arbeitsstunde
- Maximum: Joshua mit 57,8 langen Anrufen/Stunde
- Beispiel: Janis = (33,8/57,8) × 100 = 58,5%

**Langer Qualitätswert:**
- Verbindungsrate für lange Anrufe
- Maximum: Robin mit 83,5% Verbindungsrate für lange Anrufe
- Beispiel: Janis = (78,5/83,5) × 100 = 94,0%

#### Endgültige Rentabilitätswerte für lange Anrufe:
- **Robin: 86,7** = (0,40 × 91,2) + (0,30 × 74,4) + (0,30 × 100)
- **Janis: 84,1** = (0,40 × 100) + (0,30 × 58,5) + (0,30 × 94,0)
- **Joshua: 79,5** = (0,40 × 62,5) + (0,30 × 100) + (0,30 × 90,0)
- **Iris: 65,3** = (0,40 × 57,4) + (0,30 × 45,0) + (0,30 × 90,1)

### 2.2 Spezifische Metriken für lange Anrufe

**Prozentsatz langer Anrufe:**
- Formel: (Anrufe >1 Min / Gesamte verbundene Anrufe) × 100
- Ergebnisse:
  - Robin: 80,0% (540/675)
  - Iris: 79,8% (340/426)
  - Janis: 75,0% (592/790)
  - Joshua: 64,7% (370/572)

**Analyse der durchschnittlichen Anrufdauer:**
- Berechnet aus Gesamtanrufzeit / Anzahl der Anrufe
- Durchschnittswerte langer Anrufe:
  - Iris: 2m 11s (höchstes Engagement)
  - Janis: 1m 45s
  - Robin: 1m 21s
  - Joshua: 1m 02s (knapp über Schwellenwert)

### 2.3 Graphenanalyse für lange Anrufe

#### 2.3.1 Vergleich langer Anrufe (Balkendiagramm)
- Zeigt absolute Zahlen von Anrufen >1 Minute
- Hebt Qualität vs. Quantität Kompromiss hervor

#### 2.3.2 Verbindungsrate langer Anrufe (Balkendiagramm)
- Höhere Raten zeigen bessere Zielausrichtung für bedeutungsvolle Gespräche
- Robins 83,5% deutet auf exzellente Qualifizierungsfähigkeiten hin

#### 2.3.3 Wöchentliche Trends langer Anrufe (Liniendiagramm)
- Ähnliches Muster wie Gesamtanrufe, aber mit Fokus auf Qualitätsinteraktionen
- Nützlich zur Verfolgung der Engagement-Qualität über Zeit

#### 2.3.4 Verteilung langer Anrufe (Ringdiagramm)
- Gesamt: 1.842 lange Anrufe (74,8% aller Anrufe)
- Zeigt die Fähigkeit des Teams, Kunden zu binden

---

## Abschnitt 3: Konversionsraten-Erfolg Analytik

### 3.1 Verkaufsleistungsmetriken

**Produktkategorien:**
- **Object List:** Premium-Produktlinie (höherer Wert)
- **GNV:** Standard-Produktlinie (volumenbasiert)

### 3.2 Formel für Konversionseffektivität

```
Konversionseffektivität = Verkaufte Produkte / (Anrufstunden × Anrufeffizienz)
```

Diese Metrik balanciert Verkaufsleistung gegen investierte Zeit.

### 3.3 Schlüssel-Verkaufsmetriken

#### 3.3.1 Berechnung der Einheiten pro Stunde
- Formel: Gesamte verkaufte Einheiten / Gesamte Anrufstunden
- Ergebnisse:
  - Joshua: 146,9 Einheiten/Stunde (940 Einheiten / 6,4 Stunden)
  - Robin: 27,1 Einheiten/Stunde (342 Einheiten / 12,6 Stunden)
  - Janis: 19,4 Einheiten/Stunde (339 Einheiten / 17,5 Stunden)
  - Iris: 15,3 Einheiten/Stunde (267 Einheiten / 13,1 Stunden)

#### 3.3.2 Verkaufseffizienz
- Misst Konversionsqualität relativ zur aufgewendeten Zeit
- Berechnung berücksichtigt sowohl Produktmix als auch Volumen
- Ergebnisse:
  - Robin: 91% (beste ausgewogene Leistung)
  - Joshua: 89% (hohes Volumen, Einzelproduktfokus)
  - Janis: 83% (gute Balance)
  - Iris: 78% (geringere Effizienz)

### 3.4 Graphenanalyse für Konversion

#### 3.4.1 Produktverkaufsvergleich (Gestapeltes Balkendiagramm)
- **Zweck:** Visualisierung des Produktmix pro Mitarbeiter
- **Schlüsselerkenntnisse:**
  - Joshua: Extreme Spezialisierung (25 Object List, 0 GNV)
  - Robin: GNV-Spezialist (12 GNV vs 2 Object List)
  - Janis & Iris: Ausgewogener Ansatz (4-5 von jedem)

#### 3.4.2 Einheiten pro Anrufstunde (Balkendiagramm)
- **Berechnung:** Gesamteinheiten / Anrufstunden
- **Joshuas Dominanz:** 146,9 Einheiten/Stunde ist 5,4× nächstbester
- **Erkenntnis:** Spezialisierung führt zu höherem Volumen

#### 3.4.3 Verkaufsmix (Ringdiagramm)
- **Gesamteinheiten:** 1.888 (1.403 Object List + 485 GNV)
- **Verteilung:**
  - Joshua Object List: 49,8% (940/1.888)
  - Robin GNV: 14,2% (269/1.888)
  - Andere: Ausgewogenere Beiträge

#### 3.4.4 Verkaufseffizienz vs Anrufzeit (Streudiagramm)
- **X-Achse:** Gesamte Anrufstunden (investierte Anstrengung)
- **Y-Achse:** Verkaufseffizienz-Prozentsatz (Konversionsqualität)
- **Haupterkenntnis:** Umgekehrte Beziehung - weniger Zeit korreliert mit höherer Effizienz
- **Interpretation:** Fokussierte, kürzere Interaktionen können effektiver sein

### 3.5 Vergleichende Leistungsmultiplikatoren

**Joshuas Object List Vorsprung:** 5,7×
- Berechnung: 25 Produkte / 4,4 Durchschnitt andere = 5,7×

**Robins GNV-Einheiten Vorsprung:** 22,4×
- Berechnung: 269 Einheiten / 12 Durchschnitt andere = 22,4×

**Joshuas Einheiten/Stunde Vorsprung:** 2,9×
- Berechnung: 146,9 / 50,6 Teamdurchschnitt = 2,9×

**Robins Effizienzvorsprung:** 13%
- Berechnung: 91% - 78% (vs niedrigste) = 13 Prozentpunkte

### 3.6 Strategische Erkenntnisse

1. **Spezialisierung vs Diversifizierung:**
   - Joshuas fokussierter Ansatz erzielt höchstes Volumen
   - Robins GNV-Fokus zeigt Marktsegment-Beherrschung
   - Ausgewogener Ansatz (Janis/Iris) bietet Flexibilität, aber niedrigere Spitzen

2. **Zeiteffizienz-Paradoxon:**
   - Niedrigste Anrufstunden (Joshua: 6,4) → Höchste Produktivität
   - Deutet darauf hin, dass Qualität der Interaktion mehr zählt als Quantität

3. **Produkt-Markt-Passung:**
   - Verschiedene Produkte erfordern unterschiedliche Verkaufsansätze
   - Object List profitiert möglicherweise von schnellem, hochvolumigem Ansatz
   - GNV erfordert möglicherweise mehr Beziehungsaufbau

---

## Fazit

Der dreistufige Analytikansatz zeigt:

1. **Volumen ≠ Rentabilität:** Hohe Anrufzahlen garantieren keine besten Ergebnisse
2. **Effizienz ist König:** Anrufe pro Stunde ist der stärkste Erfolgsprädiktor
3. **Spezialisierung gewinnt:** Fokussierte Produktstrategien übertreffen generalistische Ansätze
4. **Qualitätsmetriken zählen:** Verbindungsraten und Anrufdauer zeigen Engagement-Qualität
5. **Zeitoptimierung:** Weniger Zeit mit höherer Intensität führt zu besseren Ergebnissen

Das Rentabilitätsbewertungssystem identifiziert erfolgreich Top-Performer durch Ausbalancierung mehrerer Faktoren und verhindert, dass eine einzelne Metrik die Bewertung dominiert.