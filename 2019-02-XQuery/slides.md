# XML-Schulung Teil II: Transformationen und Abfragen

mit XSLT und XQuery zu PDF und anderen Visualisierungen

<small>Mathias Göbel, SUB Göttingen, 12.02.2019 @ GCDH</small>

--

+ Transformationen (in Oxygen, XSLT)
+ Abfragen (in Oxygen, XQuery)
+ Abfragen einer XML-Datenbank (eXist-db, XQuery)
---
+ TEI
+ XPath
+ XML

--

## Anwendungsfälle

+ PDFs erzeugen
  + Publikation
  + Überprüfung
  + Kollationierung

+ Informationen…
  * …ex­tra­hie­ren
  * …aggregieren
  * …filtern
  * …manipulieren

--

und:

+ Anwendungen bauen
+ Suchfunktionen etablieren
+ APIs bauen

--

![XML Tree](img/XML-Baum.png)

--

![XPath Axes](img/XPath-Achsen.png)

---

## Transformationen
Die TEI unterbreitet <span class="fragment highlight-red">Vorschläge</span> zur
Visualisierung der XML-Dokumente: [die TEI-Stylesheets](https://github.com/TEIC/Stylesheets)

Sie finden auch Verwendung bei Oxgarage. <!-- .element: class="fragment" -->

--

### Zielformate
Mit XSLT oder XQuery können wir XML-Dokumente in beliebige andere Formate
umwandeln. Dabei können wir auch nach belieben filtern. Die Ausgaben sind in
vielen Fällen gut anpassbar.

--

### Oxygen

+ `mein_tagebuch.xml` öffnen
+ in der Symbolleiste: ![icons](img/Oxygen-Transform-Icons.png)

--

### Oxygen
![Configure Transformation Scenario(s)](img/Oxygen-Transform-Dialog.png) <!-- .element: height="555" -->

--

### Apply

--

### Parameter ändern: Schritt 1
![Edit Transformation Scenario(s)](img/Oxygen-Edit-Transformation.png) <!-- .element: height="555" -->

--

### Parameter ändern: Schritt 2
![Edit Transformation Scenario(s)](img/Oxygen-Edit-Scenario.png)

--

### Parameter ändern: Schritt 3
![Edit Parameters](img/Oxygen-XSLT-Parameter-Injection.png)

--

### Übung
Schalten Sie bitte diese lästige Nummerierung der Überschriften aus.

--

### Übung
Wenden Sie bitte das Transformationsszenario «TEI P5 - XHTML» an und berichten
Sie, was passiert.

--

<!-- .slide: style="color:lightgray;" -->
### Processing Instruction <!-- .element: style="color:lightgray;" -->
Ist dies in Oxygen konfiguriert gibt es praktisch keinen Mehrwert für Externe.
Die Konfiguration an sich ist nicht nachhaltig gespeichert. Daher können wir
diese auch in das XML-Dokument schreiben. Dazu dienen *processing instructions*.
```xml
<?xml-stylesheet type="text/xsl" href="path/to/xslt.xsl"?>
```

--

## XQuery

--

### FLOWR
```xquery
for $w in $list-of-words
order by $w
return
$w
```

--

![TEI Application on the Web](img/TEI-Anwendungen.png)

--

## Referenzen

[W3C XQuery Specification](https://www.w3.org/TR/xquery-31/)

[FunctX (incl. XPath functions)](http://www.xqueryfunctions.com/)

--

## Lesenswertes

Walmsley, Priscilla. 2016. XQuery, 2nd Edition. [Chapter 1 for free](http://www.datypic.com/books/xquery/9781491915103_sampler.pdf)

--

## Probierenswertes

[w3schools.com XQuery Tutorial](https://www.w3schools.com/xml/xquery_intro.asp)
