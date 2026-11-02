## Task 5 : Find a Dataset

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
