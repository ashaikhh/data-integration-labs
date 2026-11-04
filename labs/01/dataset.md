## Task 5 · Find a Dataset

### Where I searched

| Source | Kind | Search terms | Result |
|---|---|---|---|
| [FFA Marktdaten](https://www.ffa.de/marktdaten.html) | Website of the publisher | Kinobesucher, Jahreszahlen, Kinoergebnisse | Kinoergebnisse 2000–2025 mit Besucherzahl, Einnahmen und Ticketpreisen, aber nur als PDF |
| [FFA Top 50 Filme 2025](https://www.ffa.de/files/dokumentenverwaltung/studien%20mafo/2026/FFA_Top-50-Filme_2025.pdf) | Website of the publisher | Top 50 Filme | Erfolgsreichste Filme pro Jahr, nach Besucherzahl, PDF |
| [Wikidata](https://www.wikidata.org/) | Knowledge base | Das perfekte Geheimnis, The Perfect Secret | Pro Film u.a. Genre, Herkunftsland, Erscheinungsdatum und Regie; maschinenlesbar, Lizenz CC0 |
| [Open-Data-Portal München](https://opendata.muenchen.de/dataset/monatszahlen-kinos) | City or state portal | Kinos, Kinobesucher | Datensatz "Monatszahlen Kinos": monatliche Kinobesuche in München ab 2019 als CSV, Lizenz Datenlizenz Deutschland Namensnennung 2.0 |
| [GovData](https://www.govdata.de/suche/daten/kinos-leinwande-sitzplatze-der-kinos-filmbesuche-durchschnittlicher-kino-eintrittspreis-einnahm) | National or international portal | Kino, Kinobesuche | 35 Treffer, com Statistischen Bundesamt als CSV/XML (Deutschland und Bundesländer, pro Jahr) |

### Search like a machine:
Query: [GovData API](https://www.govdata.de/ckan/api/3/action/package_search?q=kino&rows=1)
- **Hits (`count`):** 129. Die Website zeigt für „Kino“ nur 35 Treffer, die API sucht offenbar breiter.
- **Title of the first hit:** Kino (Stadt Norderstedt, Land Schleswig-Holstein)
- **Licence given for:** jede Datei einzeln. `license_id` ist leer, aber runter `resources` steht bei Datenlizenz Deutschland Namensnennung 2.9 (`http://dcat-ap.de/def/licenses/dl-by-de/2.0`). 

### My Choice 
Ich wähle den Datensatz [Kinos, Leinwände, Sitzplätze der Kinos, Filmbesuche, Durchschnittlicher Kino-Eintrittspreis, Einnahmen, Filmabgabe: Deutschland, Jahre](https://www.govdata.de/suche/daten/kinos-leinwande-sitzplatze-der-kinos-filmbesuche-durchschnittlicher-kino-eintrittspreis-einnahm) vom Statistischen Bundesamt. 

- Er deckt ganz Deutschland von 2000 bis 2025 ab, pro Jahr. Das passt zu unserer Frage, wie sich die Kinobesuche seit 2000 verändert haben.
- Er ist als CSV und XML maschinenlesbar und steht unter der offnen [Datenlizenz Deutschland Namensnennung 2.0](https://www.govdata.de/dl-de/by-2-0).
- Die FFA-Daten enthalten ähnliche Kennzahlen, sind aber nur als PDF verfügbar. Ob das Statistische Bundesamt die Zahlen von der FFA übernimmt, prüfe ich in Task 6.

## Task 6 · Profile the dataset

### Facts

| Field | Value |
|---|---|
| Title | Kinos, Leinwände, Sitzplätze der Kinos, Filmbesuche, Durchschnittlicher Kino-Eintrittspreis, Einnahmen, Filmabgabe: Deutschland, Jahre |
| Publisher | Statistisches Bundesamt (Destatis), auf GovData als Datenbereitsteller und veröffentlichende Stelle genannt |
| Original publisher | Sehr wahrscheinlich die Filmförderungsanstalt (FFA): Sie erhebt Besuche und Umsätze monatlich bei den Kinos über die Filmabgabe ([FFA](https://www.ffa.de/marktdaten.html)), und die Tabelle enthält das Merkmal „Filmabgabe der Kinos an die FFA“. Destatis nennt die FFA aber nicht ausdrücklich als Quelle. |
| Link or identifier | [GovData](LINK-ZUM-DATENSATZ) |
| Formats | CSV, XML |
| Size | TODO Dateien, TODO Zeilen, TODO Spalten |
| Coverage | 2000–2025, Deutschland insgesamt, pro Jahr |
| Last update | 12.10.2026 |
| Update frequency | Nicht angegeben; bei Jahresdaten vermutlich jährlich |
| Licence | [Datenlizenz Deutschland Namensnennung 2.0](https://www.govdata.de/dl-de/by-2-0) |

### Stars 

Der Datensatz erreicht ⭐⭐⭐: Er steht unter offenen Lizenz (Datenlizenz Detuschland Namensnennung 2.0) , ist strukturiert und liegt als CSV in einem offenen, nicht proprietären Format vor. 

Für den vierten Stern fehlen URIs: Einzelne Werte, Jahre oder Merkmale wie „Filmbesuche" haben keine eigene Web-Adresse, auf die andere verlinken könnten. 

💡 Vergleich zur FFA: Deren PDFs hätten **null** Sterne, weil keine offene Lizenz angegeben ist. Mit Lizenz wäre es höchsten ⭐, weil PDF nicht strukturiert ist. 

### Open the Data

Tool: LibreOffice Calc. Import mit Zeichensatz Windows-1252 und Semikolon als Trennzeichen.

| Column | Min | Max | Mean |
|---|---|---|---|
| Filmbesuche (Mill.) | 38,1 (2020) | 177,9 (2001) | 121,2 |
| Durchschnittlicher Kino-Eintrittspreis (EUR) | 5,41 (2000) | 10,05 (2025) | 7,53 |

**Empty cells:** In den Datenzeilen (2000-2025) ist keine Zelle leer. Leer sind nur Zellen im Tabellenkopf, z.B. die ersten beiden Zellen der Jahresziele. 

**Odd Thing:**
- **Enconding:** Windows-1252 statt UTF-8. Ohne passende Einstellung werden Umlaute kaputt darstellt.
- **Seperator und Dezimalzeichen:** Semikolon als Trennzeichen, Komma als Dezimalzeichen (152,5) typisch für deutsche CSV.Dateien.
- **Struktur:** Die Tabelle ist „queer": Jahre stehen als Spalten, Merkmale als Zeilen. Für die Analyse muss ich sie umdrehen (eine Zeile pro Jahr).
- **Kopf- und Fußzeichen:** Oben stehen 6 Zeilen mit Titel, unten Quelle, Anmerkungen und Copyright. Die gehören nicht zu den Daten.
- **Einheiten:** stehen in einer eigenen Spalte (Anzahl, Mill., EUR, Mil.EUR). Filmbesuche sind in Millionen angegeben, nicht als ganze Zahl.
- **Brüche in der Zeitreihe:** Laut Fußnote sind Kinos, Leinwände und Sitzplätze 2019 und ab 2025 nicht mit den Vorjahren vergleichbar, weil die Zählweise geändert wurde. 
