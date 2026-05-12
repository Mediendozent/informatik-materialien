# Lehrerhandbuch – EDUBreakout Verschlüsselung
**Nur für Lehrkräfte – enthält alle Lösungen**

---

## Lösungen im Überblick

| Rätsel | Methode | Verschlüsselt | Klartext | Antwort |
|---|---|---|---|---|
| 1 | Caesar +3 | `GHLQ FRGH-EXFKVWDEH LVW: K` | `DEIN CODE-BUCHSTABE IST: H` | **H** |
| 2 | Atbash | `WVRM XLWV-YFXHSGZYV RHG: Z` | `DEIN CODE-BUCHSTABE IST: A` | **A** |
| 3 | Morsecode | `-.-.` | `C` | **C** |
| 4 | Binärcode | `1011` | Dezimal 11 → 11. Buchstabe | **K** |

**Finales Passwort: HACK**

---

## Rätsel 1 – Caesar-Verschlüsselung

**Prinzip:** Jeder Buchstabe wird um 3 Stellen nach rechts verschoben (Verschiebung +3).

**Entschlüsselung Buchstabe für Buchstabe:**

```
G→D  H→E  L→I  Q→N  (DEIN)
F→C  R→O  G→D  H→E  (CODE)
E→B  X→U  F→C  K→H  V→S  W→T  D→A  E→B  H→E  (BUCHSTABE)
L→I  V→S  W→T  (IST)
K→H  (Antwort!)
```

**Wichtig:** Am Ende des Alphabets wird umgebrochen – nach Z kommt A (Z+3 = C, A-3 = X).

**Häufige Fehler der Schüler:**
- In die falsche Richtung verschieben (verschlüsseln statt entschlüsseln)
- Am Alphabetende nicht umbrechen (nach Z weiter im Alphabet statt neu bei A)

---

## Rätsel 2 – Atbash

**Prinzip:** A ↔ Z, B ↔ Y, C ↔ X, ... – jeder Buchstabe wird durch seinen „Spiegel" ersetzt.

**Vollständige Mapping-Tabelle:**

```
A↔Z  B↔Y  C↔X  D↔W  E↔V  F↔U  G↔T  H↔S
I↔R  J↔Q  K↔P  L↔O  M↔N  N↔M  O↔L  P↔K
Q↔J  R↔I  S↔H  T↔G  U↔F  V↔E  W↔D  X↔C
Y↔B  Z↔A
```

**Entschlüsselung der Nachricht:**
```
W→D  V→E  R→I  M→N  (DEIN)
X→C  L→O  W→D  V→E  (CODE)
Y→B  F→U  X→C  H→S  S→H  G→T  Z→A  Y→B  V→E  (BUCHSTABE)
R→I  H→S  G→T  (IST)
Z→A  (Antwort!)
```

**Didaktischer Hinweis:** Atbash ist *selbstinvers* – dieselbe Tabelle wird zum Ver- und Entschlüsseln verwendet. Das ist ein gutes Gesprächsthema: Was sind Vor- und Nachteile dieser Eigenschaft?

---

## Rätsel 3 – Morsecode

**Lösung:** `-.-.` = C (Strich-Punkt-Strich-Punkt)

**Warum ist -.-. der Code für C?** Der Morsecode ist nicht willkürlich, sondern nach Häufigkeit im Englischen optimiert: häufige Buchstaben (E=., T=-) haben kurze Codes, seltene Buchstaben längere.

**Didaktische Vertiefung:** SOS (··· ––– ···) ist leicht einzuprägen und ein guter Aufhänger. Man kann Schüler SOS klopfen lassen (Tisch oder Handy-Taschenlampe).

---

## Rätsel 4 – Binärcode

**Lösung:** `1011` → Dezimal **11** → **K** (11. Buchstabe)

**Rechnung:**
```
Stelle:      4    3    2    1
Stellenwert: 8    4    2    1
Binärzahl:   1    0    1    1
Ergebnis: (1×8) + (0×4) + (1×2) + (1×1)
         =  8   +   0   +   2   +   1   = 11
K = 11. Buchstabe (A=1, B=2, ..., K=11)
```

**Häufige Fehler:** Stellenwerte von links nach rechts falsch zuordnen (8 ist die linkeste Stelle bei 4-Bit-Zahlen).

---

## Hinweis-System im Spiel

Das Spiel bietet 3 Tipps pro Rätsel. Die Tipps sind abgestuft:
- **Tipp 1:** Konzeptuell – erinnert an das Prinzip
- **Tipp 2:** Rechnerisch – zeigt den Rechenweg
- **Tipp 3:** Direkte Lösung – nennt den Buchstaben

Die Anzahl genutzter Tipps wird angezeigt (`[2/3]`). Lehrkräfte können dies als informelle Einschätzung nutzen.

---

## Differenzierung

### Für schnelle Teams:
- Bonus-Aufgabe: Eigenen Namen mit Caesar +3 verschlüsseln
- Bonus-Aufgabe: Einen Satz in Morsecode übersetzen
- Direkt mit `Eigenes-Breakout-Erstellen.md` beginnen

### Für langsamere Teams:
- Tipps im Spiel nutzen (bis zu 3 pro Rätsel)
- Lehrkraft erklärt das Prinzip am Beispiel, bevor Schüler es anwenden
- Rätsel 1 und 3 sind einsteigerfreundlicher (Caesar und Morse)

### Zeitliche Anpassung:
- **30-Min-Version:** Nur Rätsel 1 und 3 (Caesar + Morse), verkürzte Reflexion
- **Doppelstunde:** Vollständiges Spiel + Eigenes-Breakout in derselben Stunde erstellen
- **Hausaufgabe:** Eigenes Rätsel zu Hause entwickeln, nächste Stunde tauschen

---

## Reflexionsfragen (Musterlösungen)

**1. Caesar vs. Atbash – Unterschied?**
Caesar verschiebt jeden Buchstaben um einen festen Wert, Atbash spiegelt das Alphabet. Gemeinsam haben beide, dass jeder Klartextbuchstabe immer den gleichen Geheimtextbuchstaben ergibt → leicht durch Häufigkeitsanalyse zu knacken.

**2. Welche Methode ist am schwersten zu knacken?**
Keine der vier Methoden ist wirklich sicher – alle sind historisch und für den schulischen Einstieg gedacht. Schüler-Antworten variieren; wichtig ist die Begründung. Morse ist kein Verschlüsselungsverfahren, sondern eine Kodierung.

**3. Warum reicht Binärcode allein nicht?**
Binär ist eine Darstellungsform, keine Verschlüsselung – wer das Prinzip kennt, kann jeden Binärtext sofort lesen. Verschlüsselung braucht einen geheimen Schlüssel, der dem Empfänger bekannt ist.

**4. Verschlüsselung im Alltag:**
HTTPS (Schloss im Browser), WhatsApp-Ende-zu-Ende-Verschlüsselung, WLAN-Passwort (WPA2), Chip auf der EC-Karte, Face-ID-Daten im Smartphone.
