Hauptziel ist es die bereits öffentlich verfügbaren Daten maschinenlesbar bereit zu stellen. In der vorgeschlagenen Struktur lassen sich beliebige Kennzahlen nach Parameter gesplittet abbilden. Neben dem IST-Zustand sind bei allen Daten auch Zeitverläufe pro Tag abbildbar.

In der aktuellen Situation erscheinen uns folgende Probleme als schwerwiegend:

 * Fehlende historische Daten (z.B. an welchem Tag wurden wieviele Tests durchgeführt?)
 * Daten nicht oder unzureichend demographisch gesplittet (z.b. Alter >64 alle in einer Gruppe)
 * Daten nur teilweise geographisch gesplittet (z.b. Tests in welchen Bundesländern?)

Als Lizenz wird CC-BY 4.0 vorgeschlagen.

## Struktur der Daten

Drei CSV-Dateien:

 * Grunddaten
 * Demographische Verteilung
 * Epidemiologische Kennzahlen

Die CSV sind mit Testdaten befüllt. Die im Beispiel ausgefüllten Daten werden bereits jetzt veröffentlicht. Sie stellen also jeweils das Minimum dar, das für diese Art von Regionen befüllt werden sollte.

## Informationen zur Befüllung und Bereitstellung

 * Die CSV-Dateien werden jeden Tag zu einem Stichzeitpunkt um die aktuellen Zahlen erweitert. D.h. es kommt täglich für jedes Gebiet eine Zeile dazu. Historische Daten sind somit vorhanden.
 * Eine Zeile für jeden Tag und jedes Gebiet (AT, Bundesländer, Bezirke).
 * Die Spalten sind pro Gebiet soweit verfügbar zu befüllen.
 * Einheitliches Datumsformat für den Zeitstempel. Z.b. ISO 8601
 * Die Dateien werden als CSV via HTTPs über eine ausfallsicheren Server zur Verfügung gestellt.
 * Die URLs der Dateien verändert sich nicht, sodass eine automatische Abholung möglich ist.
 * Nicht vorhandene Werte sind nicht auszufüllen (keine "0" eingeben sondern die Spalte leer lassen)

## Mögliche Inhaltliche Erweiterungen

Zusätzlich zu den in den CSVs gelisteten Daten erscheinen mit Blick auf andere Staaten auch nachfolgende Kennzahlen wesentlich. Diese könnten als neue Spalten in Grunddaten aufgenommen werden:

 * Neu aufgenommen - Anzahl Personen in den letzten 24h im KH aufgenommen
 * Neu entlassen - Anzahl Personen in den letzten 24h aus KH entlassen (lebend)
 * Künstliche Beatmung - Anzahl Hospitalisierte, die künstliche beatmet werden
 * ECMO - Anzahl Hospitalisierter bei denen ECMO angewandt wird
 * Anzahl KHs - Anzahl der meldenden Krankenhäuser
 * Anzahl Labors - Anzahl der meldenden Labore

Bei den demographischen Daten eine weitere Aufsplittung der Altersgruppen nach Geschlecht: "<5 Jahre, weiblich", "<5 Jahre, männlich", etc.

## Mögliche Strukturelle Erweiterungen

Um die Verarbeitung auch für nicht Techniker zu vereinfachen und um Auswertungen schneller in Excel durchführen zu können, wäre nachfolgenden Erweiterungen wünschenswert.

Eine Aufteilung des Inhalts von Grunddaten in mehrere CSVs. Zum Beispiel derart, dass jeweils ein CSV nur mit den aktuellen IST-Werten befüllt ist und ein weiteres mit den historischen Daten. Auch eine Aufsplittung nach Kennzahlen wäre denkbar - zum Beispiel ein eigenes CSV in dem nur der Zeitverlauf einer Kennzahl gelistet ist. Als Beispiel für mögliche Aufteilungen sei hier nur auf vorhandene Beispiele verwiesen:

 * Sciensano, belgisches Gesundheitsministerium https://epistat.wiv-isp.be/covid/
 * Zivilschutz Italien https://github.com/pcm-dpc/COVID-19
 * Johns Hopkins CSSE https://github.com/CSSEGISandData/COVID-19
 * privater Scrapper zu info.gesundheitsministerium.at https://github.com/statistikat/coronaDAT

Hilfreich wäre auch eine Anlieferung in einem weiteren Format wie JSON.
