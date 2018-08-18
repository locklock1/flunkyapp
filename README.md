# flunkyapp

# Ideen zum Ablauf:
----------------------------------------------------------
## Vorgänge bei der Installation:
### Tutorial
geskriptetes Spiel (man trifft im Kurpark auf Gegner, die Flunkyball spielen wollen. Wird die Herausforderung abgelehnt, wird das Spiel wieder deinstalliert)
### Profilerstellung
*Name, *Deck(Standard), *Freundesliste, *Statistik(gespielt, gewonnen, etc.)
### Menü
#### Spieler gegen Spieler
##### Freunde herausfordern
##### Gegner suchen
#### Kurpark Erkunden (Spieler gegen Computer)
KI mit Decks steigenden Anspruchs, wo jeder Sieg mit (der Wahrscheinlichkeit) einer neuen Karte belohnt wird
#### Kartensammlung
Übersicht aller Karten/ Karten die man Besitzt.
Interface, in der die Karten des Decks ausgetauscht werden können (Spieler mit Spielerkarten unterschiedlicher Saisons können mehrfach vorkommen)
#### Optionen
*Musiklautstärke    *Effektlautstärke   *Schütteln zum Werfen an/aus    *Statistik zurücksetzen
#### Freundesliste
#### Statistik
----------------------------------------------------------
## Ablauf eines Spiels:
Vor dem Spiel wird festgelegt, um wie viele Schlücke man spielt. Sobald dieser Wert bei einem Spieler 0 erreicht, hat er das Spiel gewonnen.
### Deck(s) Mischen (Zufällige Reihenfolge der Karten festlegen)
### 4 Spielerkarten und 2 Aktionskarten werden angezeigt, wovon [3] ausgetauscht werden können
### Schere, Stein, Papier - Runde (Erste Runde Schere)
Nachdem entschieden ist, wer beginnt wechseln sich die Spieler im folgenden Ablauf ab:

### Würfeln (Wert zwischen 2 und 12 generieren)
### Differenz zwischen (Würfelergebnis) und (12-Trefferquote) wird angezeigt, start eines Timers
### Durch Aktionskarten kann diese Differenz beeinflusst werden, sie verlängern den Timer um 5s.
Auch die Anzahl Schlücke, die im Falle eines Treffers getrunken werden, können beeinflusst werden.
### Ablauf des Timers: Bei treffer (Differenz = +0) werden x Schlücke abgezogen

Nach 8 Runden werden 2 neue Spielerkarten gezogen, wovon eine mit einem Spieler auf dem Feld ausgetauscht werden kann.
----------------------------------------------------------
## Attribute der Karten
### Spielerkarten:
*string name, *string team-name, *int saison, *int trefferquote, *int trinkgeschwindigkeit, *int teamgeist, *int kackquote, *bild, *Karten-ID?
(Soundeffekte für Beschwören, Treffen, Weglegen, Verfehlen, Kackquote Aktiviert, Teamgeist Aktiviert, Trinken?
### Aktionskarten:
*string name, *string effekt, *effekt effekt (aus der Effekt-datenbank?)
(Soundeffekt bei Aktivierung)
----------------------------------------------------------
