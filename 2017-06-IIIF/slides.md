# TextGrid and Fontane

@IIIF Conference, 20170608, Rome

Prof. Dr. Wolfram Horstmann, Ubbo Veentjer, Mathias Göbel

--

offering IIIF in an larger infrastructure for digital editions: http://textgrid.de

---

![TEI](img/code2.png)
typical code snippet, [C7 1r](https://fontane-nb.dariah.eu/edition.html?id=%2Fxml%2Fdata%2F16b00.xml&page=1r)

--

<!-- .slide: data-background-video="img/demo2_edit1.mp4" data-background-size="contain" -->

--

### Repository: textgridrep.org
- contains currently [314957 objects](https://textgridrep.org/search?query=*)
- [426 IIIF manifests](https://textgridlab.org/1.0/iiif/manifests/)
- made for you!

--

### Laboratory
- client software for preparing xml (TEI) documents
![code](img/code2.png) <!-- .element class="fragment" -->

--

## ![IIIF](img/iiif.png) manifest preparation
- conversion from TEI to IIIF
  - image sequence from @tei:facs
  - further metadata from TextGrid metadata objects

= IIIF for every project

--

## annotation layer (PoC)
- annotations are stored standoff
- web application provides the annotation layer

--

<!-- .slide: data-background-video="img/demo_edit1.mp4" data-background-size="contain" -->

--

![synoptic view](img/synoptic-view.png)
synoptic view of facsimile, transcription and xml code within the Fontane web application
---

## benefits
- projects dont have to setup and maintain there own image server
- even Mirador is served by TextGrid
  - integrated via iframe: see [here](https://fontane-nb.dariah.eu/mirador.html?n=C7)

---

## DARIAH-DE

TextGrid is part of the DARIAH-DE infrastructure that provides authentication
and further services supporting the digital humanities.

[https://de.dariah.eu/](https://de.dariah.eu/)
