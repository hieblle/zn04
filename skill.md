---
name: filial-monatsbericht
description: Verwende diesen Skill, wenn ich um den Filial-Monatsbericht, einen Monatsbericht der Filialen, einen Filialvergleich oder eine Ampel für die Filialen bitte. Erstellt aus dem Blatt Kennzahlen einen Monatsbericht mit Budgetabweichung, Personalkostenquote, Ampel, Gebietsleitung und offenen Kundenrückmeldungen je Filiale.
---

# Filial-Monatsbericht

Erstellt aus der Arbeitsmappe „Filialcockpit ZN04“ einen geprüften Monatsbericht für die
Verkaufsleitung: eine Zeile je Filiale für den jüngsten Monat, mit Ampel und Zusammenfassung.

## Bevor du beginnst

Lies das Blatt `.Rules` und halte dich daran (Sprache, Zahlen- und Datumsformate, Kennzahlen-
definitionen, Diagrammfarben). Widersprechen sich eine Regel hier und eine Regel in `.Rules`,
gilt `.Rules`.

Verwende die Blätter `Kennzahlen`, `Stammdaten`, `Zielwerte` und `Rückmeldungen`. Verändere
keines davon. Alle Ergebnisse kommen auf ein neues Blatt `Monatsbericht`.

## Schritte

1. Bestimme den Berichtsmonat: der jüngste Monat im Blatt `Kennzahlen`. Schreibe ihn in die
   Überschrift des Blatts `Monatsbericht`, zum Beispiel „Monatsbericht September 2026“.

2. Baue eine Tabelle mit einer Zeile je Filiale und diesen Spalten, alle per Formel (XVERWEIS,
   SUMMEWENNS, ZÄHLENWENNS), nicht als eingetippte Werte:
   - `Filiale`, `Vertriebsformat`, `Filialgebietsleitung` (aus `Stammdaten`)
   - `Umsatz netto`, `Umsatz Budget`, `Budgetabweichung` = Umsatz ÷ Budget − 1
   - `Personalkostenquote` = Personalkosten ÷ Umsatz netto
   - `Ziel Personalkostenquote` (aus `Zielwerte`, je Vertriebsformat)
   - `Umsatz Vormonat` und `Veränderung zum Vormonat` = Umsatz ÷ Umsatz Vormonat − 1
     (fehlt der Vormonat, leer lassen und in der Zusammenfassung erwähnen)
   - `Negative Rückmeldungen` = Anzahl Rückmeldungen der Filiale im Berichtsmonat mit
     Bewertung 1 oder 2 (aus `Rückmeldungen`)
   - `Ampel` nach der Logik im Blatt `Zielwerte`: Grün, Gelb oder Rot. Wird kein Zielwert
     gefunden, lass die Ampel leer und nenne die Filiale in der Zusammenfassung, statt zu raten.

3. Sortiere die Tabelle nach `Budgetabweichung` aufsteigend, sodass die schwächsten Filialen
   oben stehen. Kopfzeile fixieren, Spaltenbreiten anpassen, Ampel als farbige Zelle
   (Grün, Gelb, Rot), negative Abweichungen laut `.Rules` in Klammern und rot.

4. Ergänze unter der Tabelle einen Block `Top 3 / Bottom 3` nach Budgetabweichung, mit
   Filiale, Abweichung in Prozent und Euro.

5. Füge ein gruppiertes Säulendiagramm ein: Umsatz netto gegenüber Umsatz Budget je Filiale
   für den Berichtsmonat, Farben laut `.Rules`. Der Titel nennt die Aussage
   (zum Beispiel „Vier Filialen liegen unter Budget“), nicht die Kennzahl.

6. Schreibe über die Tabelle eine Zusammenfassung mit höchstens fünf Punkten:
   - Anzahl Filialen über und unter Budget, Summe Umsatz gegenüber Summe Budget in Euro
   - die größte positive und die größte negative Abweichung, mit Filiale und Euro-Betrag
   - Filialen mit Ampel Rot und der Grund (Personalkostenquote oder Umsatz)
   - Filialen mit den meisten negativen Rückmeldungen im Berichtsmonat
   - Datenhinweise: fehlende Zielwerte, fehlender Vormonat, Auffälligkeiten, die auf
     einen Datenfehler hindeuten (zum Beispiel eine Personalkostenquote, die doppelt so hoch
     ist wie in den Nachbarmonaten)

## Regeln für die Zusammenfassung

Nenne zu jeder Aussage die Zahl, auf der sie beruht. Empfiehl keine personellen Konsequenzen
und beschreibe keine Marktleitung als leistungsschwach – berichte die Zahlen und überlasse die
Bewertung der Verkaufsleitung. Wenn eine Spalte im Blatt `Hinweis` einen Grund nennt
(zum Beispiel Teilschließung oder Parkplatzsanierung), führe ihn bei der Filiale an.
