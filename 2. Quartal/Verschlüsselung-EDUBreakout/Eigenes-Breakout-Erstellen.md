# Erstelle dein eigenes EDUBreakout!
**Informatik | Verschlüsselung | Klasse 7**

Du hast gerade vier Verschlüsselungsmethoden kennengelernt. Jetzt bist du dran: Erstelle ein eigenes Rätselspiel, das andere lösen sollen!

---

## Dein Werkzeugkasten: Die 4 Verschlüsselungsmethoden

### 1. Caesar-Verschlüsselung (Buchstabenverschiebung)

Verschiebe jeden Buchstaben um eine feste Anzahl von Stellen nach rechts.

| Verschiebung | A wird zu | B wird zu | Z wird zu |
|---|---|---|---|
| +1 | B | C | A |
| +3 | D | E | C |
| +13 (ROT13) | N | O | M |

**Selbst ausprobieren – verschlüssle mit +3:**
```
Klartext:      A B C D E F G H I J K L M
Geheimtext:    D E F G H I J K L M N O P

Klartext:      N O P Q R S T U V W X Y Z
Geheimtext:    Q R S T U V W X Y Z A B C
```

Mein Klartext:    _ _ _ _ _ _ _ _ _ _

Mein Geheimtext: _ _ _ _ _ _ _ _ _ _

---

### 2. Atbash (Spiegelcode)

Das Alphabet wird gespiegelt: A ↔ Z, B ↔ Y, C ↔ X ...

```
Klartext:   A B C D E F G H I J K L M
Geheimtext: Z Y X W V U T S R Q P O N

Klartext:   N O P Q R S T U V W X Y Z
Geheimtext: M L K J I H G F E D C B A
```

**Tipp:** Dieselbe Tabelle funktioniert zum Ver- und Entschlüsseln!

Mein Klartext:    _ _ _ _ _ _ _ _ _ _

Mein Geheimtext: _ _ _ _ _ _ _ _ _ _

---

### 3. Morsecode

```
A .-      B -...    C -.-.    D -..     E .
F ..-.    G --.     H ....    I ..      J .---
K -.-     L .-..    M --      N -.      O ---
P .--.    Q --.-    R .-.     S ...     T -
U ..-     V ...-    W .--     X -..-    Y -.--
Z --..
```

**Trennung:** Buchstaben werden durch ein Leerzeichen getrennt, Wörter durch ` / `.

Beispiel: `HACK` = `.... .- -.-. -.-`

Mein Klartext:    _ _ _ _ _ _ _ _ _ _

Mein Geheimtext: _ _ _ _ _ _ _ _ _ _

---

### 4. Binärcode (Alphabetposition)

Jeder Buchstabe hat eine Nummer (A=1, B=2, ... Z=26). Diese Nummer wird in Binär umgewandelt.

**Stellenwerte:** 16 | 8 | 4 | 2 | 1

| Buchstabe | Nummer | Binär |
|---|---|---|
| A | 1 | 00001 |
| B | 2 | 00010 |
| E | 5 | 00101 |
| K | 11 | 01011 |
| Z | 26 | 11010 |

**Selbst berechnen:** Schreibe die Nummer in Binär, indem du prüfst, welche Stellenwerte „passen":
- Passt 16 rein? Ja → schreibe 1, Rest: Zahl minus 16. Nein → schreibe 0.
- Passt 8 rein? Usw.

---

## Vorlage: Mein eigenes EDUBreakout

### Schritt 1: Rahmengeschichte erfinden

Wer ist der Bösewicht? Was wurde gesperrt? Was ist das Ziel?

```
Rahmengeschichte:
_______________________________________________
_______________________________________________
_______________________________________________

Das finale Passwort / der finale Code lautet:
_______________________
```

---

### Schritt 2: Rätsel planen (mindestens 3)

Plane deine Rätsel von hinten nach vorne: Erst das Passwort festlegen, dann die Buchstaben/Zahlen auf die Rätsel verteilen.

**Rätsel 1**

```
Verschlüsselungsmethode: ________________________________

Klartext (was soll entschlüsselt werden?):
_______________________________________________

Geheimtext (was sehen die Spieler?):
_______________________________________________

Code-Buchstabe / -Zahl als Antwort: _______
```

**Rätsel 2**

```
Verschlüsselungsmethode: ________________________________

Klartext:
_______________________________________________

Geheimtext:
_______________________________________________

Code-Buchstabe / -Zahl als Antwort: _______
```

**Rätsel 3**

```
Verschlüsselungsmethode: ________________________________

Klartext:
_______________________________________________

Geheimtext:
_______________________________________________

Code-Buchstabe / -Zahl als Antwort: _______
```

**Rätsel 4 (optional)**

```
Verschlüsselungsmethode: ________________________________

Klartext:
_______________________________________________

Geheimtext:
_______________________________________________

Code-Buchstabe / -Zahl als Antwort: _______
```

---

### Schritt 3: Lösungsblatt (nur für die Lehrkraft / das andere Team)

```
Rätsel 1: _______ Rätsel 2: _______ Rätsel 3: _______ Rätsel 4: _______

Finales Passwort: _______________________
```

---

## Checkliste: Ist mein Breakout fertig?

Bevor du dein Breakout einem anderen Team gibst, überprüfe:

- [ ] Ich habe eine Rahmengeschichte mit klarem Auftrag
- [ ] Ich habe mindestens 3 Rätsel mit verschiedenen Methoden
- [ ] Ich habe jeden Geheimtext selbst gegengeprüft (kann ich ihn entschlüsseln?)
- [ ] Das finale Passwort ergibt sich logisch aus den einzelnen Code-Buchstaben
- [ ] Ich habe ein Lösungsblatt für die Lehrkraft / das andere Team erstellt
- [ ] Die Rätsel werden von leicht nach schwer sortiert

---

## Ideen für Rahmengeschichten

Wenn dir keine Idee kommt, hier ein paar Vorschläge:

- Ein Roboter hat die Schulmensa gesperrt – ihr müsst das Menü entschlüsseln
- Ein Zeitreisender hat einen Hinweis hinterlassen, welches Datum ihr besuchen sollt
- Der Schulcomputer wurde „upgegraded" und kennt nur noch verschlüsselte Befehle
- Ein Geheimdienstagent braucht eure Hilfe, eine Nachricht zu entschlüsseln
- Eine verschlüsselte Schatzkarte führt zum versteckten Schatz im Schulgebäude

---

## Tipps für gute Rätsel

**Gut:**
- Der Geheimtext enthält einen Satz, der die Antwort klar benennt: „Dein Code-Buchstabe ist: X"
- Die verwendete Methode wird im Rätsel kurz erklärt
- Die Antwort ist eindeutig (genau ein Buchstabe oder eine Zahl)

**Problematisch:**
- Mehrdeutige Antworten (vermeiden!)
- Zu langer Text zum Entschlüsseln (max. 1–2 Sätze)
- Keine Erklärung der Methode – Spieler können ohne Vorwissen nicht lösen
