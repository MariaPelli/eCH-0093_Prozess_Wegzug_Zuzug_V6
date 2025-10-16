[//]: # (Dieser Kommentar wird nicht gerendert und bleibt nur im Raw/Edit sichtbar.)
[//]: # (Du kannst mehrere Zeilen anlegen, am besten pro Zeile einen Eintrag.)
[hidden-note]: <> (Interne Notiz: diese Definition wird nicht angezeigt, nur im Raw sichtbar)

<img src="Bilder/logo.svg" alt="Logo eCH" width="260" align="right">

# eCH-0093 – Prozess Wegzug / Zuzug

[Kontakt](./Kontakt.md) | [Hilfe](./Hilfe.md) | [Exportieren](./Exportieren.md)

> Diese README folgt dem SAGA-Layout: **Startseite/Übersicht** oben, gefolgt vom **vollständigen Inhalt**.  
> Alle Texte wurden beibehalten; die Feedback-Links sind kompakt dargestellt.

## 🌐 Übersicht der Kapitel

### 1. Einleitung 4
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [1 Einleitung 4](#1-einleitung-4)
- [1 1 Status 4](#1-1-status-4)
- [1 2 Anwendungsgebiet 4](#1-2-anwendungsgebiet-4)
### 2. Grundsätze 5
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [2 Grundsätze 5](#2-grundstze-5)
- [2 1 Notation 5](#2-1-notation-5)
- [2 2 Allgemeine Grundsätze 5](#2-2-allgemeine-grundstze-5)
- [2 3 Prozesse für den Austausch von Meldungen 5](#2-3-prozesse-fr-den-austausch-von-meldungen-5)
- [2 4 Zu liefernde Daten 6](#2-4-zu-liefernde-daten-6)
- [2 4 1 Obligatorische Daten pro Meldung 6](#2-4-1-obligatorische-daten-pro-meldung-6)
- [2 4 2 Angabe von Identifikatoren für Personen 6](#2-4-2-angabe-von-identifikatoren-fr-personen-6)
- [2 4 3 Angabe von Beziehungen 6](#2-4-3-angabe-von-beziehungen-6)
### 3. Spezifikation 6
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [3 Spezifikation 6](#3-spezifikation-6)
- [3 1 Prozesse 6](#3-1-prozesse-6)
- [3 1 1 Prozess bei direkter Meldung zwischen den Einwohnerdiensten (Hauptwohnsitz) 6](#3-1-1-prozess-bei-direkter-meldung-zwischen-den-einwohnerdiensten-hauptwohnsitz-6)
- [3 1 1 1 Teilprozess Wegzug 7](#3-1-1-1-teilprozess-wegzug-7)
- [3 1 1 2 Teilprozess Zuzug 7](#3-1-1-2-teilprozess-zuzug-7)
- [3 1 2 Prozess für Nebenwohnsitz -Begründung und -Auflösung 7](#3-1-2-prozess-fr-nebenwohnsitz-begrndung-und-auflsung-7)
- [3 1 2 1 Teilprozess Nebenwohnsitz begründen 8](#3-1-2-1-teilprozess-nebenwohnsitz-begrnden-8)
- [3 1 2 2 Teilprozess Verlän gerung Nebenwohnsitz 8](#3-1-2-2-teilprozess-verln-gerung-nebenwohnsitz-8)
- [3 1 2 3 Teilprozess Nebenwohnsitz auflösen 9](#3-1-2-3-teilprozess-nebenwohnsitz-auflsen-9)
- [3 2 Ereignismeldungen 9](#3-2-ereignismeldungen-9)
- [3 2 1 Wegzug 9](#3-2-1-wegzug-9)
- [3 2 1 1 Person – moveOutPerson 10](#3-2-1-1-person-moveoutperson-10)
- [3 2 1 1 1 Zivilstandsinformationen – maritalInfo 13](#3-2-1-1-1-zivilstandsinformationen-maritalinfo-13)
- [3 2 1 1 2 Ist eVoter – isEvoter 13](#3-2-1-1-2-ist-evoter-isevoter-13)
- [3 2 1 1 3 Ablaufdatum der Biometriedaten – biometricDataExpiryDa te 13](#3-2-1-1-3-ablaufdatum-der-biometriedaten-biometricdataexpiryda-te-13)
- [3 2 1 2 Ziel – destination 13](#3-2-1-2-ziel-destination-13)
- [3 2 1 2 1 Angaben zur Zuzugsgemeinde – moveOutReportingDestination 14](#3-2-1-2-1-angaben-zur-zuzugsgemeinde-moveoutreportingdestination-14)
- [3 2 1 3 Erweiterung – extension 14](#3-2-1-3-erweiterung-extension-14)
- [3 2 2 1 Person – moveInPerson 15](#3-2-2-1-person-moveinperson-15)
- [3 2 2 2 Meldegemeinde – hasMainResidence 15](#3-2-2-2-meldegemeinde-hasmainresidence-15)
- [3 2 3 Tod 16](#3-2-3-tod-16)
- [3 2 4 Ereignismeldungen Nebenwohnsitz 17](#3-2-4-ereignismeldungen-nebenwohnsitz-17)
- [3 2 5 Ausweis für Nebenwohsitz – secondaryResidencePermit 17](#3-2-5-ausweis-fr-nebenwohsitz-secondaryresidencepermit-17)
- [3 2 5 1 Person mit Nebenwohnsitz – secondaryResidencePermitPerson 18](#3-2-5-1-person-mit-nebenwohnsitz-secondaryresidencepermitperson-18)
- [3 2 6 Zuzug Nebenwohnsitz – moveInSecondaryResidence 21](#3-2-6-zuzug-nebenwohnsitz-moveinsecondaryresidence-21)
- [3 2 6 1 Nebenwohnsitz – secondaryRe sidence 21](#3-2-6-1-nebenwohnsitz-secondaryre-sidence-21)
- [3 2 7 Wegzug Nebenwohnsitz – moveOutSecondaryResidence 22](#3-2-7-wegzug-nebenwohnsitz-moveoutsecondaryresidence-22)
- [3 2 8 Umzug innerhalb Nebenwohsitz – moveSecondaryResidence 22](#3-2-8-umzug-innerhalb-nebenwohsitz-movesecondaryresidence-22)
- [3 2 9 Änderung Personendaten an Nebenwohnsitzgemeinde --](#3-2-9-nderung-personendaten-an-nebenwohnsitzgemeinde)
- [3 2 10 Antwortmeldung – eventReport 24](#3-2-10-antwortmeldung-eventreport-24)
### 4. Sicherheitsüberlegungen 25
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [4 Sicherheitsüberlegungen 25](#4-sicherheitsberlegungen-25)
### 5. Haftungsausschluss/Hinweise auf Rechte Dritter 26
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [5 Haftungsausschluss/Hinweise auf Rechte Dritter 26](#5-haftungsausschlusshinweise-auf-rechte-dritter-26)
### 6. Urheberrechte 26
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [6 Urheberrechte 26](#6-urheberrechte-26)
### 1. Einleitung 4
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [1 1 Status](#1-1-status)
- [1 2 Anwendungsgebiet](#1-2-anwendungsgebiet)
### 2. Grundsätze 5
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [2 1 Notation](#2-1-notation)
- [2 2 Allgemeine Grundsätze](#2-2-allgemeine-grundstze)
- [2 3 Prozesse für den Austausch von Meldungen](#2-3-prozesse-fr-den-austausch-von-meldungen)
- [2 4 1 Obligatorische Daten pro Meldung](#2-4-1-obligatorische-daten-pro-meldung)
- [2 4 2 Angabe von Identifikatoren für Personen](#2-4-2-angabe-von-identifikatoren-fr-personen)
- [2 4 3 Angabe von Beziehungen](#2-4-3-angabe-von-beziehungen)
### 3. Spezifikation 6
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [3 Spezifikation](#3-spezifikation)
- [3 1 Prozesse](#3-1-prozesse)
- [3 1 1 Prozess bei direkter Meldung zwischen den Einwohnerdiensten (Hauptwohnsitz)](#3-1-1-prozess-bei-direkter-meldung-zwischen-den-einwohnerdiensten-hauptwohnsitz)
- [3 1 1 1 Teilprozess Wegzug](#3-1-1-1-teilprozess-wegzug)
- [3 1 1 2 Teilprozess Zuzug](#3-1-1-2-teilprozess-zuzug)
- [3 1 2 Prozess für Nebenwohnsitz -Begründung und -Auflösung](#3-1-2-prozess-fr-nebenwohnsitz-begrndung-und-auflsung)
- [3 1 2 1 Teilprozess Nebenwohnsitz begründen](#3-1-2-1-teilprozess-nebenwohnsitz-begrnden)
- [3 1 2 2 Teilprozess Verlängerung Nebenwohnsitz](#3-1-2-2-teilprozess-verlngerung-nebenwohnsitz)
- [3 1 2 3 Teilprozess Nebenwohnsitz auflösen](#3-1-2-3-teilprozess-nebenwohnsitz-auflsen)
- [3 2 Ereignismeldungen](#3-2-ereignismeldungen)
- [3 2 1 Wegzug](#3-2-1-wegzug)
- [3 2 1 1 Person – moveOutPerson](#3-2-1-1-person-moveoutperson)
- [3 2 1 1 3](#3-2-1-1-3)
- [3 2 1 1 2 Ist eVoter – isEvoter](#3-2-1-1-2-ist-evoter-isevoter)
- [3 2 1 1 3 Ablaufdatum der Biometriedaten – biometricDataExpiryDate](#3-2-1-1-3-ablaufdatum-der-biometriedaten-biometricdataexpirydate)
- [3 2 1 2 Ziel – destination](#3-2-1-2-ziel-destination)
- [3 2 1 2 1 Angaben zur Zuzugsgemeinde – moveOutReportingDestination](#3-2-1-2-1-angaben-zur-zuzugsgemeinde-moveoutreportingdestination)
- [3 2 1 3 Erweiterung – extension](#3-2-1-3-erweiterung-extension)
- [3 2 2 1 Person – moveInPerson](#3-2-2-1-person-moveinperson)
- [3 2 2 2 Meldegemeinde – hasMainResidence](#3-2-2-2-meldegemeinde-hasmainresidence)
- [3 2 3 Tod](#3-2-3-tod)
- [3 2 4 Ereign ismeldungen Nebenwohnsitz](#3-2-4-ereign-ismeldungen-nebenwohnsitz)
- [3 2 5 Ausweis für Nebenwohsitz – secondaryResidencePermit](#3-2-5-ausweis-fr-nebenwohsitz-secondaryresidencepermit)
- [3 2 5 1 Person mit Nebenwohnsitz – secondaryResidencePermitPerson](#3-2-5-1-person-mit-nebenwohnsitz-secondaryresidencepermitperson)
- [3 2 6 1 Nebenwohnsitz – secondaryResidence](#3-2-6-1-nebenwohnsitz-secondaryresidence)
- [3 2 8 Umzug innerhalb Nebenwohsitz – move SecondaryResidenc e](#3-2-8-umzug-innerhalb-nebenwohsitz-move-secondaryresidenc-e)
- [3 2 9 Änderung Personendaten an Nebenwohnsitzgemeinde -- changePersonInform ationTo-](#3-2-9-nderung-personendaten-an-nebenwohnsitzgemeinde-changepersoninform-ationto)
- [3 2 10 Antwortmeldung – eventReport](#3-2-10-antwortmeldung-eventreport)
### 4. Sicherheitsüberlegungen 25
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [4 Sicherheitsüberlegungen](#4-sicherheitsberlegungen)
### 6. Urheberrechte 26
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [6 Urheberrechte](#6-urheberrechte)
### 3. Spezifikation 6
- Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.0-blue)
- [3 1 2 2 T](#3-1-2-2-t)
- [3 2 8 22 Neue Meldung für Umzug innerhalb Nebenwohnsitzge-](#3-2-8-22-neue-meldung-fr-umzug-innerhalb-nebenwohnsitzge)
- [3 2 5 17 Die Meldung für die Begründung eines Nebenwohnsitzes](#3-2-5-17-die-meldung-fr-die-begrndung-eines-nebenwohnsitzes)
- [3 1 2 7 Die Prozessbeschreibung für Begründung und A uflösung](#3-1-2-7-die-prozessbeschreibung-fr-begrndung-und-a-uflsung)
- [3 2 9 23 Es wu rde eine neue Meldung für die Information der Ne-](#3-2-9-23-es-wu-rde-eine-neue-meldung-fr-die-information-der-ne)
- [3 2 5 17 Die Meldung eventSecondaryResidencePermit wurde um](#3-2-5-17-die-meldung-eventsecondaryresidencepermit-wurde-um)
- [3 2 10 24 Es wurde die Möglichkeit für die Übergabe einer negati-](#3-2-10-24-es-wurde-die-mglichkeit-fr-die-bergabe-einer-negati)
- [3 2 1 1 3 13 Mit der Meldung für die Begründu ng des Aufenthalts](#3-2-1-1-3-13-mit-der-meldung-fr-die-begrndu-ng-des-aufenthalts)
- [3 2 1 1 1 13 Neu können auch die zusätzlichen Zivilstandsangaben](#3-2-1-1-1-13-neu-knnen-auch-die-zustzlichen-zivilstandsangaben)
- [3 2 1 1 2 13 Neu kann mit der Meldung moveOut auch das Flag ist](#3-2-1-1-2-13-neu-kann-mit-der-meldung-moveout-auch-das-flag-ist)

---
# eCH-0093 – Prozess Wegzug / Zuzug

> Dieses README enthält den **gesamten Standard** in einer einzigen Datei, nach Kapiteln gegliedert.  
> Für **jedes Unterkapitel** ist eine **Versionsnummer** (hier: 4.0.0) angegeben sowie **Feedback-Links**.

**Quelle:** eCH-0093 – Prozess Wegzug / Zuzug, Version 4.0.0, Entwurf, Ausgabedatum 2022-04-21.  
**Hinweis zu Links:** Ersetze `OWNER/REPO` oben in den Feedback-Links durch deine GitHub-Organisation bzw. dein Repo.

---

Hinweis
Aus Gründen der besseren Lesbarkeit und Verständlichkeit wird im vorliegenden Dokument bei der
Bezeichnung von Personen ausschliesslich die maskuline Form verwendet. Diese Formulierung
schliesst Frauen in ihrer jeweiligen Funktion ausdrücklich mit ein.

eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 1 Einleitung

---
**Feedback**: [Ankündigungen von eCH](https://github.com/MariaPelli/eCH-0093_Prozess_Wegzug_Zuzug_V6/discussions/categories/announcements) · [Fehler melden][bug-6] · [Verbesserung vorschlagen](https://github.com/MariaPelli/eCH-0093_Prozess_Wegzug_Zuzug_V6/discussions/categories/Ideas) · [Alle Issues][issues-6] · [Diskussionen][discuss-6]

---
<a id="1-1-status-4"></a>
### 1 1 Status · Version: ![v4.0.0](https://img.shields.io/badge/version-4.0.2-blue)

Entwurf: Das Dokument wurde von den zuständigen Referenten aus dem Expertenausschuss zur
öffentlichen K onsultation freigegeben und entsprechend publiziert.
Vorschlag: Das Dokument wird dem Ex pertenausschuss zur Genehmigung vorgelegt, ist aber nor-
mativ noch nicht gültig.
Genehmigt: Das Dokument wurde vom Expertenausschuss genehmigt. Es hat für das definierte Ein-
satzgebiet im festgelegten Gültigkeitsbereich normative Kraft.

Frühere Versionen: [v4.0.1](4.0.1) · [v4.0.0](4.0.0)

---
**Feedback**: [Fehler melden][bug-1] · [Verbesserung vorschlagen][feat-1] · [Alle Issues][issues-1] · [Diskussionen][discuss-1]

---
<a id="1-2-anwendungsgebiet-4"></a>
### 1 2 Anwendungsgebiet · Version: `4 0 0`
Die Einwohnerdienste haben den gesetzlichen Auftrag, Einwohnerregister zu führen und die regi-
strierten und geänderten Personendaten den berechtigten Verwaltungsst ellen zu melden. Das vorlie-
gende Dokument spezifiziert
- den Prozess für den Austausch von Wegzugs, respektive Zuzugsmeldungen zwischen den
betroffenen Einwohnerdienste ,
- die vorgesehenen Meldegründe,
- und die Daten, welche bei Eintreten der entsprechenden E reignisse weiterzugeben sind.
Im vorliegenden Dokument nicht behandelt werden Problem - und Spezialfälle wie z.B.:
- Eine Person zieht in eine andere Gemeinde zu als jene, welche sie in ihrer Wegzugsgemeinde
angegeben hat.
- eine Person zieht weg ohne sich abz umelden.
- Die Zuzugsgemeinde weigert sich, eine zuziehende Person anzumelden.
- Die Wegzugsgemeinde weigert sich die wegziehende Person abzumelden.
Der Standard geht davon aus, dass derartige Spezialfälle wie bisher manuell behandelt werden. Sie
werden daher nicht spezifiziert.
Zudem wird die Praxis von den Gemeinden unterschiedlich gehandhabt. Manche Gemeinden neh-
men Personen erst definitiv auf, wenn eine Reihe von Vorbedingungen erfüllt ist, andere ziehen es
vor, Personen erst einmal definitiv anzumelden und allenfalls später die Anmeldung zu annullieren.
Der vorgeschlagene Standard lässt somit Raum für unterschiedliche Vorgehensweisen in den Ge-
meinden.
Im vorliegenden Dokument nicht behandelt werden Ereignismeldungen, welche bereits im Standard
eCH-0020 besc hrieben sind.
Es werden nur Daten berücksichtigt, welche:
- in den Basis -Standards eCH-0011, eCH -0044 und eCH -0021 geführt werden

Frühere Versionen: [v4.0.1](4.0.1) · [v4.0.0](4.0.0)

---
**Feedback**: [Fehler melden][bug-1] · [Verbesserung vorschlagen][feat-1] · [Alle Issues][issues-1] · [Diskussionen][discuss-1]

[bug-1]: ./1.2/kap-1-2_bug.md
[feat-1]: ./1.2/kap-1-2_feature.md
[issues-1]: ./1.2/kap-1-2_issues.md
[discuss-1]: ./1.2/kap-1-2_discussions.md


---
<a id="2-1-notation-5"></a>
### 2 1 Notation · Version: `4 0 0`
Die Richtlinien in diesem Dokument werden gemäss der Terminologie aus [RFC2119] angegeben,
dabei kommen die folgenden Ausdrücke zur Anwendung, die durch GROSSSCHREIBUNG als Wör-
ter mit den folgenden Bedeutungen kenntlich gemacht wer -den:
ZWINGEND: Der Ver antwortliche muss die Vorgabe umsetzen.
EMPFOHLEN: Der Verantwortliche kann aus wichtigen Gründen auf eine Umsetzung der Vor-
gabe verzichten.
OPTIONAL: Es ist dem Verantwortlichen überlassen, ob er die Vorgabe umsetzen will.

Frühere Versionen: [v4.0.1](4.0.1) · [v4.0.0](4.0.0)

---
**Feedback**: [Fehler melden][bug-2] · [Verbesserung vorschlagen][feat-2] · [Alle Issues][issues-2] · [Diskussionen][discuss-2]

---
### 2 2 Allgemeine Grundsätze · Version: `4 0 0`
Bezüglich der Meldung von Ereignissen aus dem Bereich der Einwohnerdienste sind folgende
Grundsätze einzuhalten:
 [ZWINGEND], Sowohl der Zuzug wie auch der Wegzug sind über Ereignisse zu melden.
 [ZWINGEND], Jede Meldung enthält nur die Daten zu einer Person .
 [EMPFHOHLEN] Sollen mehrere rechtlich zusammengehörige Personen gemeinsam gemel-
det werden, so sind die einzelnen Personenmeldungen mittels eCH -0058 zu bündeln.
 [ZWINGEND], Die identifizierenden Merkmale sind immer zu liefern.
 [ZWINGEND] , grundsätzlich i st bei Attributen immer der Wert nach dem Ereignis zu liefern.
Abweichende Sachverhalte sind explizit bei den entsprechenden Ereignismeldungen festge-
halten.
 [ZWINGEND] Es sind immer alle bekannten Informationen mit dem Ereignis zu lie fern auch
wenn das entsprechende Element optional ist.
 [ZWINGEND] Ein optionales Element darf nicht leer geliefert werden. Ist die Information nicht
bekannt darf das optionale Element nicht übergeben werden.
Beispiel Gültigkeit bei Ausländerkategorie.
 [ZWINGEND] Umzugsmeldungen, welche den gleichen Haushalt betreffen, müssen mittels
der gleichen Geschäftsfall -Identifikation,
eCH-0058:headerType:businessProcessID als zusammengehörig gekennzeichnet werden.
 [ZWINGEND] Bei der Weitergabe von Umzugsmeldungen (Wegzug / Zuzug) die aus eUmzug
stammen – erkennbar am Präfix „EUMZUG“ in der businessProcessID – ist die businessPro-
cessID aus eUmzug weiterzugeben.

---
**Feedback**: [Fehler melden][bug-2] · [Verbesserung vorschlagen][feat-2] · [Alle Issues][issues-2] · [Diskussionen][discuss-2]

---
### 2 3 Prozesse für den Austausch von Meldungen · Version: `4 0 0`
Die Detail -Prozesse auf Anwendungsebene für das Übermitteln und Konsumie ren von Ereignismel-
dungen sind in [eCH -0058] beschrieben.


E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 2.4 Zu liefernde Daten

---
**Feedback**: [Fehler melden][bug-2] · [Verbesserung vorschlagen][feat-2] · [Alle Issues][issues-2] · [Diskussionen][discuss-2]

---
### 2 4 1 Obligatorische Daten pro Meldung · Version: `4 0 0`
Jede Ereignismeldung wird zusammen mit generellen Informationen gemeldet. Dazu gehörten insbe-
sondere das Ereignisdatum sowie Sperrvermerke. Die Informationen sind in [eCH -0058] beschrieben.

---
**Feedback**: [Fehler melden][bug-2] · [Verbesserung vorschlagen][feat-2] · [Alle Issues][issues-2] · [Diskussionen][discuss-2]

---
### 2 4 2 Angabe von Identifikatoren für Personen · Version: `4 0 0`
Wird in den nachfolgend beschriebenen Ereignismeldungen von ‚Personenidentifikatoren gemäss
eCH-0044’ gesprochen, so sind immer alle identifizierenden Merkmale gemeint. D ies gilt im Besonde-
ren für die Merkmale Name , Vorname (n), Geschlecht und Geburtsdatum .

---
**Feedback**: [Fehler melden][bug-2] · [Verbesserung vorschlagen][feat-2] · [Alle Issues][issues-2] · [Diskussionen][discuss-2]

---
### 2 4 3 Angabe von Beziehungen · Version: `4 0 0`
Bei der Meldung von Ereignissen sind grundsätzlich nur jene Beziehungen zu anderen Personen zu
melden, welche im Kontext der entsprechenden Meldun g von Bedeutung sind.
Wird in den einzelnen Beschreibungen der Meldegründe von ‚Beziehung zu "xyz“’ gesprochen, so
sind immer alle notwendigen Attribute damit gemeint. Dabei können die Angaben zur Identifizierung
der betroffenen Person
entweder
durch Ang abe der identifizierenden Merkmale (Schlüsselattribute)
oder
durch Angabe einer vollständigen Wohnadresse
erfolgen.

---
**Feedback**: [Fehler melden][bug-2] · [Verbesserung vorschlagen][feat-2] · [Alle Issues][issues-2] · [Diskussionen][discuss-2]

---
### 3 Spezifikation · Version: `4 0 0`
---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 Prozesse · Version: `4 0 0`
---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 1 Prozess bei direkter Meldung zwischen den Einwohnerdiensten (Hauptwohnsitz) · Version: `4 0 0`
Die nachfolgende Grafik zeigt den Prozess für den Austausch von Weg - respektive Zuzugsmeldun-
gen zwischen den betroffenen Einwohnerdiensten , sowie die daraus resultierenden Ereignismeldun-
gen. In Anschluss an die Beschreibung, ist der gleiche Prozess auch no ch in Form eines BPMN -Dia-
gramms aufgeführt. Der Todesfall wird nachfolgend nicht aufgeführt, da bei Todesfällen nur eine Mel-
dung an ggf. vorhandene Nebenwohnsitzgemeinden erfolgt.


E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 1: UML -Diagramm zum Prozess WegZug / Zuzug (eine grössere Version ist im Anhang zu finden)

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 1 1 Teilprozess Wegzug · Version: `4 0 0`
Die Person meldet sich beim Einwohnerdienst der aktuellen Gemeinde ab (person deregisters with
destination Swiss municipality) .
[ZWINGEND] Wird beim Wegzug eine Schweizer Gemeinde al s Zielort (Zuzugsgemeinde) angege-
ben, so meldet der Einwohnerdienst nach vollständig abgeschlossenem Wegzug diesen an die ange-
gebene Zuzugsgemeinde (Message moveOut) .
Welche Daten die Wegzugsmeldung beinhaltet ist im Kapitel 3.2.1 ersichtlich.
[EMPFOHLEN] Sind weitere Verwaltungsstellen über den Wegzug zu informieren, so meldet dies die
Wegzugsgemeinde mittels der entsprechenden eCH -0020 -Ereignismeldungen (Message eCH-
0020: moveOut) .

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 1 2 Teilprozess Zuzug · Version: `4 0 0`
Die Person meldet sich beim Einwohnerdienst der Zuzugsgemeinde an (Person registers with move
in municipality) .
[ZWINGEND] Ist die Person aus einer anderen Schweizer Gemeinde zugezogen, so meldet die Zu-
zugsgemeinde den definitiv erfolgten Zuzug der Wegzugsgemeinde (Message moveIn) .
Welche Daten die Zuzugsmeldung beinhaltet ist im Kapitel 3.2.2 ersichtlich.
[EMPFOHLEN] Sind weit ere Verwaltungsstellen über den Zuzug zu informieren, so meldet dies die
Zuzugsgemeinde mittels der entsprechenden eCH -0020 -Meldegründe (Message eCH -0020:moveIn) .

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 2 Prozess für Nebenwohnsitz -Begründung und -Auflösung · Version: `4 0 0`
Die nachfolgende Grafik zeigt den Prozess für den Austausch der Meldungen im Zusammenhang mit
Nebenwohnsitz zwischen der Hauptwohnsitzgemeinde und der Nebenwohnsitzgemeinde.




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 2: Prozesse im Kontext von Nebenwohnsitz

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 2 1 Teilprozess Nebenwohnsitz begründen · Version: `4 0 0`
Die meldepflichtige Person meldet sich beim Einwohnerdienst der Hauptwohnsitzgemeinde und bean-
tragt einen "Ausweis auswärtigen Aufenthalt " (Application for weekly residence) um damit in einer an-
deren Gemeinde einen Nebenwohnsitz zu begründen.
Die Hauptwohnsitz gemeinde informiert die Nebenwohnsitzgemeinde hinsichtlich der Bewilligung mit-
tels der Meldung "Ausweis für Nebenwohnsitz" (secondaryResidencePermit) . Welche Daten die Mel-
dung enthält ist im Kapitel 3.2.5 ersichtlich.
Die meldepflichtige Person meldet sich beim Einwohnerdienst der Nebenwohnsitzgemeinde an (re-
gistration with secondary residence municipality) .
Die Nebenwohnsitzgemeinde informiert die Hauptwohnsitzgeme inde über die Begründung des Ne-
benwohnsitzes mit der Meldung "Zuzug Nebenwohnsitz" (moveInSecondaryResidence) . Welche Da-
ten die Meldung enthält ist im Kapitel 3.2.6 ersichtlich.

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 2 2 Teilprozess Verlängerung Nebenwohnsitz · Version: `4 0 0`
Die Nebenwohnsitzgemeinde informiert die meldepflichtige Person , vor Ablauf des Ausweises, einen
neuen Ausweis zu liefern.
Die meldepflichtige Person bestellt die Verlängerung bei der Hauptwohnsitzgemeinde.
Die Hauptwohnsitzgemeinde informiert die Nebenwohnsitzgemeinde hinsichtlich der Verlängerung



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 der Bewilligung mittels der Meldung "Ausweis für Nebenwohnsitz" (secondaryResidencePermit). Wel-
che Daten die Meldung enthält ist im Kapitel 3.2.5 ersichtlich.
Die Nebenwohnsitzgemeinde erfasst die Verl ängerung. Es findet kein "neue Zuzug" statt.
Die Nebenwohnsitzgemeinde informiert die Hauptwohnsitzge meinde, im Sinne einer Quittung, mit der
Meldung "Zuzug Nebenwohnsitz" (moveInSecondaryResidence). Welche Daten die Meldung enthält
ist im Kapitel 3.2.6 ersichtlich.

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 2 3 Teilprozess Nebenwohnsitz auflösen · Version: `4 0 0`
Die meldepflichte Person meldet beim Einwohnerdienst der Nebenwohnsitzgemeinde, dass sie den
Nebenwohnsitz auflösen will.
Die Nebenwohnsitzgeme inde informiert die Hauptwohnsitzgemeinde mit der Meldung "Wegzug Ne-
benwohnsitz" über die Auflösung des Nebenwohnsitzes. Welche Daten die Meldung enthält ist im Ka-
pitel 3.2.7 ersichtlich.
Die Auflösung des Nebenwohnsitzes kann von der meldepflichtigen Person auch bei der Hauptwohn-
sitzgemeinde gemeldet werden. In diesem Falle sendet die Hauptwohnsitzgemeinde der Nebenwohn-
sitzgemeinde die Meldung "Wegzug Nebenwohnsitz" . Welche Daten die Meldung enthält ist im Kapi-
tel 3.2.7 ersichtlich.

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 Ereignismeldungen · Version: `4 0 0`
Sofern in den nachfolgenden Spezifikationen, sowie in den als Anhang vermerk ten Dokumenten,
nicht explizit ein bestimmter Basisstandard für ein Element erwähnt ist, gelten die Definitionen ge-
mäss eCH -0011

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 Wegzug · Version: `4 0 0`
Präfix moveOut

Ereignisbeschreibung:
Die Wegzugsgemeinde meldet der, von der wegziehenden Person als Zielort genannte n, Zu-
zugsgemeinde den erfolgten Wegzug.
Ereignisdaten
Folgende Informationen zur weggezogenen Person sind beim Eintreten des Ereignisses zu
übermitteln:
 Person (zwingend) – moveOutPerson, siehe Kapitel 3.2.1.1
 Ziel (zwingend) – destination , siehe Kapitel 3.2.1.1.1
 Erweiterung (optional) – extension, siehe K apitel 3.2.1.3



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 3 eventMoveOutType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 Person – moveOutPerson · Version: `4 0 0`
Die detaillierten Angaben zu den einzelnen Datentypen sind in den Basiss tandards [eCH -
0044], [eCH -0011] und [eCH -0021] beschrieben.
Ereignisdaten
Folgende Informationen werden übermittelt :
 Personenidentifikatoren (zwingend) – personIdentification, siehe
eCH-0044:personIdentificationType
 Namensangaben (zwingend) – nameData, siehe eCH -0011:nameDataType
 Geburtsangaben (zwingend) – birthData, siehe eCH -0011:birthDataType
 Geburtszusatzangaben (optional) – birthAddonData, siehe
eCH-0021:birthAddonDataType
 Staatsangehörigkeitsangaben (zwingend) – nationalityData, siehe
eCH-0011:nationalityDataType
 Zustelladresse (optional) – addressForService, siehe
eCH-0011:contactDataType
 Konfessionsangaben (optional) – religionData, siehe
eCH-0011:religionDataType
 Zivilstandsinformationen (zwingend) – maritalInfo , siehe Kapitel 3.2.1.1.1
entweder
o Heimatortangaben (zwingend, mehrfach) – placeOfOrigin, siehe eCH -
0011:placeOfOriginType
oder
o Ausländerkategorie (zwingend) – residencePermitData, siehe eCH -0011:resi-
dencePermitDataType
 Personenzusatzdaten (optional) – personAdditionalData, siehe eCH -0021:personAddi-
tionalData
 Angaben zur beruflichen Tätigkeit (optional) – jobData, siehe eCH -0021:jobDataType
 Zivilsta ndsbeziehung (optional) – maritalRelationship, siehe eCH -0021:maritalRelati-
onshipType



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21  Elternbeziehung (optional, mehrfach) – parentalRelationship, siehe eCH -0021:paren-
talRelationshipType
 Kindes - und erwachsenenschutzrechtliche Beziehung (optional, mehrfach ) – guardian-
Relationship, siehe eCH -0021:guardianRelationshipType
 Militärdienstpflichtangaben (optional) – armedForcesData, siehe eCH -0021:armed-
ForcesDataType
 Zivilschutzdienstpflichtangaben (optional) – civilDefenseData, siehe eCH -0021:civilDe-
fenceDataTyp e
 Wehrdienstpflicht - / Feuerwehrdienstpflichtangaben (optional) – fireServiceData, siehe
eCH-0021:fireServiceDataType
 Krankenversicherungsangaben (optional) – healthInsuranceData, siehe eCH -
0021:healthInsuranceDataType
 Güter - und/oder erbrechtliche Vereinb arungen (optional) – matrimonialInheritanceAr-
rangementData, siehe eCH -0021: matrimonialInheritanceArrangementDataType
 Sperrvermerke (optional) – lockData, siehe eCH -0021:lockDataType
 Ist eVoter (optional) – isEvoter, siehe Kapitel 3.2.1.1.2
 Ablaufdatum der Biometriedaten (optional) – biometricDataExpiryDate, siehe Kapitel

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 3 · Version: `4 0 0`
 Nebenwohnsitz (optional, mehrfach) – secondaryResidence, siehe eCH -0007:swiss-
MunicipalityType






E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 4: moveOutPersonType (grössere Version im Anhang)



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 3.2.1.1.1 Zivilstandsinformationen – maritalInfo
Angaben zum Zivilstand
Ereignisdaten
Folgende Informationen werden übermittelt :
 Zivilstandsangaben (zwingend) – maritalData, siehe eCH -0011:maritalDataType
 Zivilstandszusatzangaben (optional) – maritalDataAddon, siehe eCH-0021:mari-
talDataAddonType


Abbildung 5: maritalInfoType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 2 Ist eVoter – isEvoter · Version: `4 0 0`
Angabe, ob die Person als eVoter registriert ist oder nicht, respektive an Urnengängen elektro-
nisch teilnehmen will.
True = Person ist eVoter
False = Person ist nicht eVoter

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 3 Ablaufdatum der Biometriedaten – biometricDataExpiryDate · Version: `4 0 0`
Ablaufdatum der Biometriedaten.

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 2 Ziel – destination · Version: `4 0 0`
Angaben zum Zuzug.

Ereignisdaten
Folgende Informationen werden übermittelt :
 Angaben zur Zuzugsgemeinde (zwingend) – moveOutReportingDestination, siehe Ka-
pitel 3.2.1.2.1




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 6 destinationType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 2 1 Angaben zur Zuzugsgemeinde – moveOutReportingDestination · Version: `4 0 0`
Angaben zur Zuzugsgemeinde.

Ereignisdaten
Folgende Informationen werden übermittelt:
 Meldegemeinde (zwingend) – reportingMunicipality, siehe
eCH-0007:swissMunicipalityType
 Zuzugsgemeinde ( optional ) – destinationMunicipality, siehe
eCH-0007:swissMunicipalityType
 Zuzugsadresse (zwingend) – destinationAddress
entweder
unbekannt (zwingend) – unknown
oder
Schweizer Gemeinde (zwingend) – swissTown, siehe
eCH-0011:dwellingAddressType
oder
Ausland (zwingend) – foreignCountry, siehe
eCH-0010:addressInformationType
 Wegzugsdatum (zwingend) – departureDate, xs:date
 Zuzugsort (optional) – comesFrom, siehe eCH -0011:destinationType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 3 Erweiterung – extension · Version: `4 0 0`
Erweiterungspunkt für die Übe rmittlung kantonal spezifischer, im Standard nicht explizit defi-
nierter Daten.

[ZWINGEND] Die Nutzung muss zwischen den Schnittstellenpartnern geregelt werden.



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 3.2.2 Zuzug
Präfix moveIn

Ereignisbeschreibung:
Die Zuzugsgemeinde meldet der Wegzugsgemeinde den erfolgten Zuzug.
Ereignisdaten
Folgende Informationen zur zugezogenen Person sind beim Eintreten des Ereignisses zu
übermitteln.
 Person (zwingend) – moveInPerson, siehe Kapitel 3.2.2.1
 Meldegemeinde (zwingend) – hasMainResidence, siehe Kapitel 3.2.2.2
 Erweiterung (optional) – extens ion, siehe Kapitel 3.2.1.3


Abbildung 7 eventMoveInType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 2 1 Person – moveInPerson · Version: `4 0 0`
Die Detailangaben zu „personIdentification“ sind im [eCH -0044] ersichtlich.
Ereignisdaten
Folgende Information en werden übermittelt .
 Personenidentifikatoren (zwingend) – personIdentification, siehe eCH -0044:per-
sonIdentificationType

Abbildung 8 oveInPersonType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 2 2 Meldegemeinde – hasMainResidence · Version: `4 0 0`
Die Detailangaben zu den einzelnen Elemente n sind in den Basisstandards [eCH -0007] und
[eCH -0011] ersichtlich.
Ereignisdaten
Folgende Informationen werden übermittelt .



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21  Meldegemeinde (zwingend) – reportingMunicipality, siehe eCH -0007:swissMunicipality
 Zuzugsdatum (zwingend) – arrivalDate
 Zuzugsort ( optional) – comesFrom, siehe eCH -0007:swissMunicipalityType
 Wohnadresse (zwingend) – dwellingAddress
Entweder
unbekannt (zwingend) – unknown
oder
Schweizer Gemeinde (zwingend) – swissTown, siehe
eCH-0011:dwellingAddressType
oder
Ausland (zwingend) – foreignCountry, siehe
eCH-0010:addressInformationType


Abbildung 9 moveInReportingMunicipalityType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 3 Tod · Version: `4 0 0`
Präfix death

Ereignisbeschreibung: Information von bekannten Nebenwohnsitzgemeinden bezüglich Tod
einer im Register eingetragenen Person.
Ereignisdaten
Folgende Informationen zur verstorbenen Person sind beim Eintreten des Ereignisses an die
Nebenwohnsitzgemeinden zu übermitteln:
 Person (zwingend) – deathPerson, siehe eCH -0044:personIdentification Type
 Todesdatum (zwingend) – dateOfDeath
 Erweiterung (optional) – extension, siehe Kapitel 3.2.1.3




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 10 eventDeathType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 4 Ereign ismeldungen Nebenwohnsitz · Version: `4 0 0`
Für die elektronische Abwicklung der Prozesse im Bereich Nebenwohnsitz sind, vor allem auch mit
Blick auf eUmzug, die folgenden Prozesse wichtig Begründung Nebenwohnsitz , Verlängerung Neben-
wohnsitz, Umzug innerhalb Nebenwohnsitzge meinde und Auflösung Nebenwohnsitz. Der vorliegende
Standard behandelt bewusst nicht die zum Teil komplexen Abklärungen, welche im Zusammenhang
mit diesen Prozessen wichtig sind. Er definiert nur die Meldungen welche im Kontext dieser Prozesse
ausgetauscht werden können.

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 5 Ausweis für Nebenwohsitz – secondaryResidencePermit · Version: `4 0 0`
Präfix secondaryResidencePermit

Ereignisbeschreibung: Die Hauptwohnsitzgemeinde sendet der Nebenwohnsitzgemeinde
den Ausweis "Ausweis für auswärtigen Aufenthalt", damit die Nebenwohnsitzgemeinde die
Person mit Nebenwohnsitz ins Register aufnehmen kann.

Ereignisdaten
Folgende Informationen werden übermittelt .
 Person mit Nebenwohnsitz (zwingend) – secondaryResidencePermitPerson, siehe Ka-
pitel 3.2.5.1
 Angaben zum Hauptwohnsitz
o Gemeinde Hauptwohnsitz (zwingend) – destinationMunicipality, siehe eCH -
0007:swissMunicipalityType
o Adresse Hauptwohnsitz (zwingend) – destinationAdd ress, siehe eCH -
0011:dwellingAddressType
 Angaben zur Nebenwohnsitzgemeinde
o Gemeinde Nebenwohnsitz Ziel ( optional ) – destinationMunicipality, siehe eCH -
0007:swissMunicipalityType
o Adresse Nebenwohnsitz (zwingend) – destinationAddress, siehe eCH -
0011:dwellin gAddressType
 Nebenwohnsitz Bewilligung gültig ab (zwingend) – secondaryResidencePermitVa-
lidFrom
 Nebenwohnsitz Bewilligung gültig bis (optional) – secondaryResidencePermitValidTill
 Erweiterung (optional) – extension, siehe Kapitel 3.2.1.3




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21

Abbildung 11: eventSecondaryResidencePermit

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 5 1 Person mit Nebenwohnsitz – secondaryResidencePermitPerson · Version: `4 0 0`
Ereignisdaten
Folgende Informationen werden übermittelt .
 Personenidendtifikation (zwingend) – personIdentification, siehe eCH -0044:per-
sonIdentificationType
 Namensangaben (zwingend) – nameData, siehe eCH -0011:nameDataType
 Geburtsangaben (zwingend) – birthData, siehe eCH -0011:birthDataType
 Geburtszusa tzangaben (optional) – birthAddonData, siehe eCH -0021:birthAd-
donDataType
 Staatsangehörigkeit (zwingend) – nationalityData, siehe eCH -0011:nationalityDa-
taType
 Adresse für Dienstleistungen (optional) – addressForServices, siehe eCH -0011:con-
tactDataType
 Konfe ssionsangaben (optional) – religionData, siehe eCH -0011:religionDataType
 Zivilstandsinformationen (zwingend) – maritalInfo , siehe Kapitel 3.2.1.1.1
 Entweder
Heimatort (zwingend, mehrfach) – placeOfOrigin,
siehe eCH -0011:placeOfOriginType
oder
Ausländerkategorie (zwingend) – residencePermit,
siehe eCH -0011:residencePermitDataType
 Personenzusatzangaben (optional) – personAdditionalData , siehe eCH -0021:perso-
nAdditionalData
 Berufsangaben (optional) – jobData, siehe eCH -0021:jobDataType



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21  Zivilstandsbeziehung (optional) – maritalRelationshop, siehe eCH -0021:maritalRelati-
onshipType
 Elternbeziehung (optional, mehrfach) – parentalRelationship, siehe eCH -0021:paren-
talRelationshipType
 Kindes - und erwachsenenschutzrechtliche Beziehung (optional, mehrfach) – guardian-
Relationship, siehe eCH -0021:guardianRelationshipType
 Militärdienstangaben (optional) – armedForcesData, siehe eCH -0021:armedForces-
Data Type
 Zivilschutzdienstangaben (pptional) – civilDefenseData, siehe eCH -0021:civilDefense-
DataType
 Wehrdienstpflicht - / Feuerwehrdienstpflichtangaben (optional) – fireServiceData, siehe
eCH-0021:fireServiceDataType
 Krankenversicherungsangaben (optional) – healthInsuranceData, siehe eCH -
0021:healtInsuranceDataType
 Güter - und/oder Erbrechtliche Vereinbarungen (optional) – matrimonialInheritanceAr-
rangementData, siehe eCH -0021: matrimonialInheritanceArrangementDataType
 Sperrvermerke (optional) – lockData, siehe eCH-0021:lockDataType
 Nebenwohnsitz (optional, mehrfach) – secondaryResidence, siehe eCH -0007:swiss-
MunicipalityType
 Politischer Wohnsitz (optional) – politicalResidence, siehe eCH -0007:swissMunicipali-
tyType



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21

Abbildung 12: secondaryResicendePermitPersonType (grössere Version im Anhang)



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 3.2.6 Zuzug Nebenwohnsitz – moveInSecondaryResidence
Präfix moveInSecondaryResidence

Ereignisbeschreibung: Die Nebenwohnsitzgemeinde sendet der Hauptwohnsitzgemeinde
eine Bestätigung, dass die Pers on mit Nebenwohnsitz im Register aufgenommen wurde.

Ereignisdaten
Folgende Informationen werden übermittelt .

 Person (zwingend) – moveInSecondaryPerson, siehe eCH -0044:personIdentification-
Type
 Nebenwohnsitz (zwingend) – secondaryResidence, siehe Kapitel 3.2.6.1
 Erweiterung (optional) – extension, siehe Kapitel 3.2.1.3


Abbildung 13: eventMoveInSecondaryResidenceType

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 6 1 Nebenwohnsitz – secondaryResidence · Version: `4 0 0`
Ereignisdaten
Folgende Informationen werden übermittelt .
 Meldegemeinde (zwingend) – reportingMunicipality, siehe eCH -0007:swissMunicipali-
tyType
 Zuzugsdatum (zwingend) – arrivalDate
 Wohnadresse (zwingend) – dwellingAddresss, siehe eCH -0011:dwellingAddressType


Abbildung 14: secondaryResidenceType



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 3.2.7 Wegzug Nebenwohnsitz – moveOutSecondaryResidence
Präfix moveOutSecondary Residence

Ereignisbeschreibung: Die Nebenwohnsitzgemeinde sendet der Hauptwohnsitzgemeinde
eine Bestätigung, dass die Person ihren Nebenwohnsitz aufgelöst hat.

Ereignisdaten
Folgende Informationen werden übermittelt .
 Person (zwingend) – moveOutSecondaryPerson, siehe eCH -0044:personIdentification-
Type
 Wegzugsdatum (zwingend) – departureDate
 Meldegemeinde (zwingend) – reportingMunicipality, siehe eCH -0007:swissMunicipality
 Erweiterung (optional) – extension, siehe Kapitel 3.2.1.3


Abbildung 15: eventMoveOutSecondaryResidence

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 8 Umzug innerhalb Nebenwohsitz – move SecondaryResidenc e · Version: `4 0 0`
Präfix moveSecondaryResidence

Ereignisbeschr eibung: Die Nebenwohnsitzgemeinde sendet der Hauptwohnsitzgemeinde
die Angaben zur neuen Adresse innerhalb der Nebenwohnsitzgemeinde .

Ereignisdaten
Folgende Informationen werden übermittelt .
 Personenidendtifikation (zwingend) – personIdentification, siehe eCH-0044:per-
sonIdentificationType
 Gemeinde Nebenwohnsitz (zwingend) – reportingMunicipality, siehe eCH -0007:swiss-
MunicipalityType
 Adresse Nebenwohnsitz (zwingend) – dwellingAddress, siehe eCH -0011:dwellingAdd-
ressType
 Erweiterung (optional) – extension, si ehe Kapitel 3.2.1.3




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 16: eventMoveSecondaryResidence

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 9 Änderung Personendaten an Nebenwohnsitzgemeinde -- changePersonInform ationTo- · Version: `4 0 0`
SecondaryResidence
Präfix changePersonInformationToSecorndaryResidence

Ereignisbeschreibung: Die Hauptwohnsitzgemeinde sendet der Nebenwohnsitzgemeinde
Änderungen an den Personendaten.

Ereignisdaten
Folgende Informationen werden übermittelt .
 Person mit Nebenwohnsitz (zwingend) – secondaryResidencePermitPerson, siehe Ka-
pitel 3.2.5.1
 Angaben zum Hauptwohnsitz
o Gemeinde Hauptwohnsitz (zwing end) – destinationMunicipality, siehe eCH -
0007:swissMunicipalityType
o Adresse Hauptwohnsitz (zwingend) – destinationAddress, siehe eCH -
0011:dwellingAddressType
 Angaben zur Nebenwohnsitzgemeinde
o Gemeinde Nebenwohnsitz Ziel (optional) – destinationMunicipali ty, siehe eCH -
0007:swissMunicipalityType
o Adresse Nebenwohnsitz (zwingend) – destinationAddress, siehe eCH -
0011:dwellingAddressType
 Erweiterung (optional) – extension, siehe Kapitel 3.2.1.3




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 17: eventChangePersonInformationToSecondaryResidence

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 10 Antwortmeldung – eventReport · Version: `4 0 0`
Präfix eventReport

Ereignisbeschreibung: Die Antwortmeldung gibt der Nebenwohnsitzgemeinde die Möglich-
keit der Hauptwohnsitzgemeinde elektronisch zu melden, ob eine Meldung angenommen
wurde (positiveReport) oder abgelehnt wurde (negativeReport).

Ereignisdaten
Folgende Informationen werden übermittelt .
 Kopfdaten (zwingend) – header , siehe eCH-0058:headerType
Entweder
o Positive Meldung (zwingend) -- positiveReport, siehe eCH -0058:positiveReport-
Type
Oder
o Negative Meldung (zwingend) – negativeReport, siehe eCH -0058:negati-
veReportType




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 18: eventReport

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 4 Sicherheitsüberlegungen · Version: `4 0 0`
Keine.




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 5 Haftungsausschluss/Hinweise auf Rechte Dritter
eCH-Standards, welche der Verein eCH dem Benutzer zur unentgeltlichen Nutzung zur Verfügung
stellen oder welche eCH referenzier en, haben nur den Status von Empfehlu ngen. Der Verein eCH
haftet in keinem Fall für Entscheidungen ode r Massnahmen, welche der Benutzer auf Grund dieser
Dokumente trifft und / oder ergreift. Der Benutzer ist verpflichtet, die Dokumente vor deren Nutzung
selbst zu überprüfen und si ch gegebenenfalls beraten zu lassen. eCH-Standards können und sollen
die tech nische, organisatorische oder juristische B eratung im konkreten Einzelfall nicht ersetzen.
In eCH-Standards referenzierte Dokumente, Verfahren, Methoden, Produkte und Standards sind u n-
ter Umständen markenrechtlich, urheberrechtlich oder patentrechtlich ges chützt. Es liegt in der aus-
schliesslichen Verantwortlichkeit des Benutzers, sich die allenfalls erforderlichen Rechte bei den je-
weils berechtigten Personen und/oder Organisation en zu be schaffen.
Obwohl der Verein eCH all seine Sorgfalt darauf verwendet, die eCH-Standards sorgfältig auszua r-
beiten, kann keine Zusicherung oder Garantie auf Aktualität, Vollständigkeit, Richtigkeit bzw. Fehler-
freiheit der zur Verfügung gestellten Informationen und Dokumente gegeben we rden. Der Inhalt von
eCH-Standards kann jederzeit und ohne Ankündigung geändert werden.
Jede Haftung für Schäden, welche dem Benutzer aus dem Gebrauch der eCH-Standards entstehen
ist, soweit gesetzlich zulässig, wegbed ungen.

---
**Feedback**: [Fehler melden][bug-4] · [Verbesserung vorschlagen][feat-4] · [Alle Issues][issues-4] · [Diskussionen][discuss-4]

---
### 6 Urheberrechte · Version: `4 0 0`
Wer eCH-Standards erarbeitet, behält das geistige Eigentum an diesen. Allerdings verpflic htet sich
der Erarbeitende , sein betreffendes geistiges Eigentum oder seine Rechte an geistigem Eigentum a n-
derer, sofern möglich, den jeweiligen Fachgruppen und dem Verein eCH kostenlos zur uneinge-
schränkten Nutzung und Weiterentwicklung im Rahme n des Vereinszweckes zur Verfügung zu stel-
len.
Die v on den Fachgruppen erarbeiteten Standards können unter Nenn ung der jeweiligen Urheber von
eCH unentgelt lich und uneingeschränkt genutzt, weiterverbreitet und weiterentwi ckelt werden.
eCH-Standards sind vollständig dokumentiert und frei von lizenz - und/oder patentrechtlichen Ein-
schränkungen. Die dazugehörige Dokumentation kann unentgeltlich bezogen werden.
Diese Bestimmungen gelten ausschliesslich für die von eCH erarbeiteten Standards, nicht jedoch für
Standards oder Produkte Dritter, auf welche in den eCH-Standards Bezug genommen wird. Die Stan-
dards enthalten die entsprechenden Hinweise auf die Rechte Drit ter.



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 Anhang A – Referenzen & Bibliographie
[eCH -0007] Datenstandard Gemeinden, Version 5.0
[eCH -0010] Datenstandard Postadresse für natürliche Personen, Firmen, Organisatio-
nen und Behörden, Version 8.0.0
[eCH -0011] Datenstandard Personendaten, Version 9.0.0
[eCH -0020] Schnittstellenstandard Meldegründe Personenregister, Version 4.0.0
[eCH -0021] Datenstandard Personenzusatzdaten, Version 8.0.0
[eCH -0044] Datenstandard Austausch von Personenidentifikationen, Version 4.1
[eCH -0058] Schnittstellenstandard Meldungsrahmen, Version 5.0
[RFC2119] Key words for use in RFCs to Indicate Requirement Levels
[XSD] XML Schema Part 1: Structures. W3C Recommendation 2. Mai 2001.
XML Schema Part 2: Datatypes. W3C Recommendation 2. Mai 2001.
Anha ng B – Mitarbeit & Überprüfung
Walter Allemann Verband Schweizerischer Einwohnerdienste (VSED)
Andreas Bechtiger Abraxas Informatik
Angelina Düring Stadt St. Gallen
Luca Feller Axians IT&T AG
Theres Fuchs Gemeinde Gelterkinden
Viktor Geiger Kanton AG
Thomas Koller Innosolv
Benjamin Meile Innosolv
Regula Meier Bedag Informatik
Enrico Moresi Lustat Luzern
Renato Stebler Bedag Informatik
Martin Stingelin Stingelin Informatik
Daniela Sulzer Hürlimann Informatik
Max Zurkinden Bundesamt für Statistik



E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 Anhang C – Abkürzungen und Glossar
Begriff Definition
Meldegrund Ein Meldegrund ist ein Ereignis, welches Mutationen der Da-
ten im Einwohnerregister gemäss Standard eCH -0005 "Mel-
dewesen" nötig macht und zu einer Meldung an Umsysteme
führt. Mutationen, welche keine Meldung an Umsysteme zur
Folge haben, werden in diesem Dokument nicht beschrieben.
Ereignis Das Eintreten eines spezifischen Sachverhalts , zum Beispiel
einer Geburt oder das Erreichen eines bestimmten Zeitpunkts
zum Beispiel Volljährigkeit.
Ereignismeldung Meldung aller relevanten Informationen zu einem bestimmten
Meldegrund an eine oder mehrere externe Stelle.
Anhang D – Änderungen gegen über Vorversion
Änderung von Version 3.0 zu Version 4.0.0
Kapitel Seite Anpassung RFC Nr .

---
**Feedback**: [Fehler melden][bug-6] · [Verbesserung vorschlagen][feat-6] · [Alle Issues][issues-6] · [Diskussionen][discuss-6]

---
### 3 1 2 2 T · Version: `4 0 0`
eilpro-
zess
Verlän-
gerung
Neben-
wohnsitz 8 Anpassung der Prozessbeschreibung für die Verlänge-
rung Nebenwohnsitz 2020 -84

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 8 22 Neue Meldung für Umzug innerhalb Nebenwohnsitzge- · Version: `4 0 0`
meinde 2020 -83

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 5 17 Die Meldung für die Begründung eines Nebenwohnsitzes · Version: `4 0 0`
wurde um die Angaben zum politischen Wohns itz er-
gänzt. 2020 -82

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 1 2 7 Die Prozessbeschreibung für Begründung und A uflösung · Version: `4 0 0`
des Nebenwohnsitzes wurde angepasst. 2020 -81

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 9 23 Es wu rde eine neue Meldung für die Information der Ne- · Version: `4 0 0`
benwohnsitzgemeinde bei Änderung der Personendaten
aufgenommen. 2020 -80

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 5 17 Die Meldung eventSecondaryResidencePermit wurde um · Version: `4 0 0`
die Angaben zur Hauptwohnsitzgemeinde ergänzt 2020 -79


E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 Kapitel Seite Anpassung RFC Nr .

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 10 24 Es wurde die Möglichkeit für die Übergabe einer negati- · Version: `4 0 0`
ven Antwor tmeldung geschaffen 2020 -78

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 3 13 Mit der Meldung für die Begründu ng des Aufenthalts · Version: `4 0 0`
kann auch das Ablaufdatum von Biometriedaten überge-
ben werden. 2020 -50

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 1 13 Neu können auch die zusätzlichen Zivilstandsangaben · Version: `4 0 0`
gem. eCH -0021 übergeben werden. 2020 -49

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---
### 3 2 1 1 2 13 Neu kann mit der Meldung moveOut auch das Flag ist · Version: `4 0 0`
eVoter übergeben werden 2018 -45
Tabelle 1 Änderungen gegenüber Vorversion
Anhang E – Abbildungsverzeichnis
Abbildung 1: UML -Diagramm zum Prozess WegZug / Zuzug (eine grössere Version ist im Anhang zu
finden) ................................ ................................ ................................ ................................ .... 7
Abbildung 2: Prozesse im Kontext von Nebenwohnsitz ................................ .......................... 8
Abbildung 3 eventMoveOutType ................................ ................................ .......................... 10
Abbildung 4: moveOutPersonType (grössere Version im Anhang) ................................ ....... 12
Abbildung 5: maritalInfoType ................................ ................................ ............................... 13
Abbildung 6 destinationType ................................ ................................ ................................ 14
Abbildung 7 eventMoveInType ................................ ................................ ............................. 15
Abbildung 8 oveInPersonType ................................ ................................ ............................. 15
Abbildung 9 moveInReportingMunicipalityType ................................ ................................ .... 16
Abbildung 10 eventDeathType ................................ ................................ ............................. 17
Abbildung 11: eventSec ondaryResidencePermit ................................ ................................ .. 18
Abbildung 12: secondaryResicendePermitPersonType (grössere Version im Anhang) ........ 20
Abbildung 13: eventMoveInSecondaryResidenceType ................................ ........................ 21
Abbildung 14: secondaryResidenceType ................................ ................................ ............. 21
Abbildung 15: eventMoveOutSecondaryResidence ................................ ............................. 22
Abbildung 16: eventMoveSecondaryResidence ................................ ................................ ... 23


E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 Abbildung 17: eventChangePersonInformationToSecondaryResidence .............................. 24
Abbildung 18: eventReport ................................ ................................ ................................ ... 25
Abbildung 19: UML -Diagramm zum Prozess WegZug / Zuzug ................................ ............. 31
Abbildung 20 moveOutPersonType ................................ ................................ ..................... 32
Abbildung 21: secondaryResidencePermitPerson ................................ ................................ 33
Anhang F – Tabellenverzeichnis
Tabelle 1 Änderungen gegenüber Vorversion ................................ ................................ ...... 29

Anhang G – Abhängigkeiten




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21 Anhang H – Abbildungen

Abbildung 19: UML -Diagramm zum Prozess WegZug / Zuzug




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 20 moveOutPersonType




E-Government Standards



eCH-0093 – Prozess Wegzug / Zuzug / 4.0.0 / Entwurf / 2022 -04-21
Abbildung 21: secondaryResidencePermitPerson

---
**Feedback**: [Fehler melden][bug-3] · [Verbesserung vorschlagen][feat-3] · [Alle Issues][issues-3] · [Diskussionen][discuss-3]

---

---
[bug-1]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.1&title=%5BBug%5D%20Kap.1%3A%20
[feat-1]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.1&title=%5BVerbesserung%5D%20Kap.1%3A%20
[issues-1]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.1%22
[discuss-1]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.1
[bug-1]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.1&title=%5BBug%5D%20Kap.1%3A%20
[feat-1]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.1&title=%5BVerbesserung%5D%20Kap.1%3A%20
[issues-1]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.1%22
[discuss-1]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.1
[bug-1]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.1&title=%5BBug%5D%20Kap.1%3A%20
[feat-1]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.1&title=%5BVerbesserung%5D%20Kap.1%3A%20
[issues-1]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.1%22
[discuss-1]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.1
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-4]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.4&title=%5BBug%5D%20Kap.4%3A%20
[feat-4]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.4&title=%5BVerbesserung%5D%20Kap.4%3A%20
[issues-4]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.4%22
[discuss-4]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.4
[bug-5]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.5&title=%5BBug%5D%20Kap.5%3A%20
[feat-5]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.5&title=%5BVerbesserung%5D%20Kap.5%3A%20
[issues-5]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.5%22
[discuss-5]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.5
[bug-6]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.6&title=%5BBug%5D%20Kap.6%3A%20
[feat-6]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.6&title=%5BVerbesserung%5D%20Kap.6%3A%20
[issues-6]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.6%22
[discuss-6]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.6
[bug-1]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.1&title=%5BBug%5D%20Kap.1%3A%20
[feat-1]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.1&title=%5BVerbesserung%5D%20Kap.1%3A%20
[issues-1]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.1%22
[discuss-1]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.1
[bug-1]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.1&title=%5BBug%5D%20Kap.1%3A%20
[feat-1]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.1&title=%5BVerbesserung%5D%20Kap.1%3A%20
[issues-1]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.1%22
[discuss-1]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.1
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-2]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.2&title=%5BBug%5D%20Kap.2%3A%20
[feat-2]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.2&title=%5BVerbesserung%5D%20Kap.2%3A%20
[issues-2]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.2%22
[discuss-2]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.2
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-4]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.4&title=%5BBug%5D%20Kap.4%3A%20
[feat-4]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.4&title=%5BVerbesserung%5D%20Kap.4%3A%20
[issues-4]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.4%22
[discuss-4]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.4
[bug-6]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.6&title=%5BBug%5D%20Kap.6%3A%20
[feat-6]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.6&title=%5BVerbesserung%5D%20Kap.6%3A%20
[issues-6]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.6%22
[discuss-6]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.6
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
[bug-3]: https://github.com/OWNER/REPO/issues/new?labels=bug,Kap.3&title=%5BBug%5D%20Kap.3%3A%20
[feat-3]: https://github.com/OWNER/REPO/issues/new?labels=enhancement,Kap.3&title=%5BVerbesserung%5D%20Kap.3%3A%20
[issues-3]: https://github.com/OWNER/REPO/issues?q=is%3Aissue+label%3A%22Kap.3%22
[discuss-3]: https://github.com/OWNER/REPO/discussions?discussions_q=Kap.3
