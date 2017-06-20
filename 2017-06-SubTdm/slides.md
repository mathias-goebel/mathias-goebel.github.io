# TDM @ SUB

Text Mining als Teil der Datenanalyse an der SUB

<small>SUB Planungsgruppe, 20170620, Göttingen</small>

---

## Text Mining

»Erkennung von Bedeutungsstrukturen in unstrukturierten Textdaten« (Wikipedia)
\+ Ermittlung von Kennzahlen und weiteren Metadaten aus Textdaten und Analyse
dieser.

--

### unstrukturierte Textdaten der SUB

- Volltexte des GDZ (OCR)
- Digitale Editionen
- TextGrid Repository
- Nationallizenzen
<hr/> <!-- .element: class="fragment" data-fragment-index="1" -->
- GOEDOC <!-- .element: class="fragment" data-fragment-index="1" -->
- erworbene E-Medien <!-- .element: class="fragment" data-fragment-index="1" -->

--

### Bedeutungsstrukturen

- inhaltsbezogene Schlagwörter
  - Kollokationen
  - Topic Modeling
- genannte Entitäten (Personen, Orte/Regionen, Spezies, …)
- Disambiguierung

--

### Kennzahlen

- Type/Token-Ratio
- Readbility Scores

---

### Index

Ergebnisse des Text Minings sind Annotationen und Metadaten. Um diese nutzen zu
können, müssen wir sie in einen Index zusammenführen und diesen aktuell halten.
Daher bedarf es eines Workflows zur Erfassung neuer Produkte in einem TM-System.

---

## Zentrale Anlaufstelle Text Mining

- Verarbeitung eigener/lizenzierter Dokumente
- Mehrwertdienste aus einzelnen Verarbeitungsschritten generieren und anbieten

--

### Beispiel Tokenizer

Python NLTK ist eine State of the Art Programmbibliothek für Natural Language
Processing. Der Tokenizer scheitert aber an Guillemets (», «) und daraus
entstehen Folgefehler in allen weiteren Verarbeitungsschritten.
