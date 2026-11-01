# Open Source: pandas

Repository: [pandas-dev/pandas](https://github.com/pandas-dev/pandas)

## Licence 
- **Licence file:** [BSD 3-Clause License](https://github.com/pandas-dev/pandas/blob/main/LICENSE)
- **Permissive or copyleft:** Permisive. Die [BSD 3-Clause License](https://github.com/pandas-dev/pandas/blob/main/LICENSE) erlaubt Nutzung, Änderung und Weitergabe, auch kommerziell, ohne dieselbe Lizenz haben muss.  
- **If I copy code into my project:** Ich muss den Copyright-Hinweis und den Lizenztext mitkopieren, und ich darf den Namen pandas nicht ohne Erlaubnis nutzen, um für mein Projekt zu werben ([License](https://github.com/pandas-dev/pandas/blob/main/LICENSE))

## What machines see 
| Repository | `spdx_id` | Explanation |
|---|---|---|
| [pandas-dev/pandas](https://api.github.com/repos/pandas-dev/pandas) | `BSD-3-Clause` | GitHUb erkennt die Lizenzdatei als BSD 3- Clause, also können auch Maschinen die Lizenz lesen. |
| [ashaikhh/data-integration-labs](https://api.github.com/repos/ashaikhh/data-integration-labs) | `MIT` | GitHub erkennt meine LICENSE-Datei als MIT-Lizenz, die ich aus dem Template erstellt habe. |
| [owid/co2-data](https://api.github.com/repos/owid/co2-data) | `null` | GitHUb findet keine Lizenzdatei, obwohl die README die Daten unter "license" stellt: Menschen sehen die Lizenz, Maschinen nicht.  |

## Community files 

| File | Present? |
|---|---|
| README | ✓ [README.md](https://github.com/pandas-dev/pandas/blob/main/README.md) |
| LICENSE | ✓ [LICENSE](https://github.com/pandas-dev/pandas/blob/main/LICENSE) |
| CONTRIBUTING | ✓ [CONTRIBUTING.md](https://github.com/pandas-dev/.github/blob/master/CONTRIBUTING.md) |
| CODE_OF_CONDUCT | ✓ [CODE_OF_CONDUCT.md](https://github.com/pandas-dev/.github/blob/master/CODE_OF_CONDUCT.md) |

CONTRIBUTING und CODE_OF_CONDUCT liegen nicht im panads-Repo selbst, sondern im gemeinsamen `.github`-Repository der Organisation panads-dev. GitHub zählt sie trotzdem für alle Repos der Organisation. Zusätzlich gibt es eine Security Policy und ein Pull-Request-Template. 

Quelle: [Community standards](https://github.com/pandas-dev/pandas/community)

## People 
- **Contributors:** über 3.887 ([Quelle](https://github.com/pandas-dev/pandas/graphs/contributors), Stand: 01.11.2026)
- **Who decides what gets merged?:** Das **Core Team**, also Contributors, die mindestens ein Jahr lang viel und gut beigetreten haben und vom Core Team gewählt wurden. Es entscheidet im Konsens über Pull Requests und die Richtung des Projekts. Darüber steht formal ein **BDFL** („Benevolent Dictator for Life“), aktuelle Wes McKinney, der Gründer von pandas. Er kann das Core Team überstimmen, tut das nur selten, z.B bei einem Patt. ([Governance](https://pandas.pydata.org/about/governance.html), [Team](https://pandas.pydata.org/about/team.html)).

## Money
pandas wird aus mehreren Quellen finanziert ([Sponsors](https://pandas.pydata.org/about/sponsors.html)):
- **Stiftung:** pandas ist ein Projekt von **NumFOCUS**, einer gemeinnützigen Stiftung in den USA. Sie verwaltet Spenden und übernimmt rechtliche und finanzielle Aufgaben.
- **Firmen, die Entwickler bezahlen:** Institutional Partner wie **Nvidia** stellen Leute an, die im Rahmen ihrer Arbeit an pandas mitarbeiten.
- **Sponsoren:** **Tidelift** und **Bodo** geben Geld.
- **Spenden:** über NumFOCUS bzw. den Bereich „Sponsor this project" auf GitHub.
- **Freiwillige:** Viele Contributors arbeiten unbezahlt mit.

Wichtig: Laut [Governance](https://pandas.pydata.org/about/governance.html) können Geldgeber die Entscheidungen des Projekts nicht kaufen. Einfluss hat nur, wer selbst mitarbeitet. 

## Activity 
- **Latest Release:** pandas 3.1.0 vom 22.10.2026 ([pandas.pydata.org](https://pandas.pydata.org/), [Release notes](https://pandas.pydata.org/docs/whatsnew/v3.1.0.html))
-  **Open issues:** **Open pull requests**

## My way in
- **How does a change get in?:** ([Contributing guide](https://pandas.pydata.org/docs/dev/development/contributing.html)):
1. Ein passendes **Issue*+ finden. Es darf noch niemand zugewiesen sein und kein Label wie `Needs Triage` oder `Needs Discussion` haben.
2. Das Issue mit dem Kommentar `/take` übernehmen. Ein Bot weist es dir zu, du darfst höchstens zwei gleichzeitig haben. 
3. Das Repo **forken**, einen eigenen Branch anlegen und die Änderung machen, inklusive Tests.
4. Einen **Pull Requests** öffnen, der das Issue verlinkt (z.B `closes #1234`) und mit einem Präfix wie `BUG:` oder `DOC:` beginnt.
5. Die automatischen Tests (CI) müssen grün sein, dann prüft ein Maintainer den Code.

Bemerkenswert: pandas hat eine eigene Regel für KI-Tools. Man darf sie nutzen, muss aber angeben, welches Tool und Modell man verwendet hat, und darf in Diskussionen nicht die KI für sich sprechen lassen. 

**Newcomer label:** 
















