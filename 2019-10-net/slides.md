<!-- .slide: data-background-iframe="https://fontane-nb.dariah.eu/tei-conf/net/" -->

# Semantic Networks in Structured Text Data

 CERL Annual Seminar 2019: Collections and Networks

<small>Mathias Göbel, SUB Göttingen, <a href="https://twitter.com/goebel_m">@goebel_m</a></small>

<small>https://mathias-goebel.github.io/2019-10-net/</small>

^Note: All slides are available online, you can see the URL at the bottom of this slide.
What I am going to present here is based on a talk held and a paper i wrote
together with Martin de la Iglesia back in 2013 where we both worked in a project
on the notebooks of a famose german author from the late 19th century: Theodor Fontane.
“Who is John Maynard?” …

--

## Credits

based on a talk held together with Martin de la Iglesia at TEI Members Meeting
and Conference 2013

prepared with data from the “<a href="https://fontane-nb.dariah.eu">Genetic-critical and annotated edition of Theodor Fontane’s notebooks</a>” and <a href="https://dracor.org">DraCor.org</a>

^Note: If we have time at the end I like to show you another example preparing
networks from dramatic texts

--

## ToC
+ Structured Text Data
+ Network Analysis
+ Outlook

---

## Structured Text Data

--

SUB Göttingen supports projects creating digital editions by

* preparing data model <!-- .element: class="fragment" -->
* designing workflow <!-- .element: class="fragment" -->
* setting up database <!-- .element: class="fragment" -->
* creating search indices <!-- .element: class="fragment" -->
* visualizing the data <!-- .element: class="fragment" -->
* archiving the results <!-- .element: class="fragment" -->

^Note: be aware of that this is not a complete list! one of the most important technology we are utilizing is made by the Text Encoding Initiative. TEI: a guideline for encoding texts.

--

We (use|support|love) TEI.

![TEI Logo](https://tei-c.org/Vault/Logos/TEIlogo.svg) <!-- .element: style="max-height:18em" -->

--

TEI is currently based on XML. XML is organized as an hierarchical structure
made of <span class="fragment highlight-red">*nodes*</span>.

^Note: …and a network is a structure made up of a set of nodes (vertices) and a
set of ties between these nodes, called edges (sometimes called links).

--

<iframe height="650" width="650" src="examples/1.html"></iframe>

--

<iframe height="650" width="650" src="examples/2.html"></iframe>

^Note: We usually refer to this formation as the “tree-like” structure…

--

<!-- .slide: data-background-image="img/Kucuk_Camlica_06465-Wikicommons-Nevit_Dilmen-CC-BY-SA3.jpg" data-background-size="contain" -->
<small style="margin-top: 67%;color:white;">“Tree at Küçük Çamlıca, Istanbul”. Nevit Dilmen from Wikimedia Commons. [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)</small>

^Note: nice image.

--

### Example

^Note: So now we want to look at the notebooks and here are the facts:

--

* PI/Editor: Dr. Gabriele Radecke
* funded by the German Research Foundation (DFG) from 2011 to 2019

^Note: …

--

* period: 1859 - 1880s
* 67 notebooks
* 64 - 120 leaves each
* < 10.000 pages

^Note: we are dealing with 10k pages to be found in 67 notebooks.

--

![Theodor Fontane: Notizbuch C7, Blatt 1r. Hrsg. von Gabriele Radecke.](img/c71r.jpg) <!-- .element: style="max-height:15em" -->

<small>[C7, 1r](https://fontane-nb.dariah.eu/test/edition.html?id=%2Fxml%2Fdata%2F16b00.xml&page=1r)</small>

^Note: This is a not randomly chosen page from the notebook with the signature C7.
There are many features to find on this page like stamps, different writing utensil (pencil and pen), different style of characters, underlines, an area marked deleted. We can find place names, persons are mentioned, dates, and much more. And we encoded all of this!

--

![transcription view](img/c71r-transcription.png) <!-- .element: style="max-height:18em" -->

^Note: Our digital version of this page represents the topographic structure of
the page.

--

```xml
<surface n="1r">
  <zone>
    <line>Luther</line>
    <line>1. Johannes Hilten (Eiſe-</line>
    <!-- … -->
  </zone>
</surface>
```

^Note: Here is an example of the first two lines from the main text of this page.

--

```xml
<surface n="1r">
  <zone>
    <line><seg><rs type="direct" ref="psn:Luther">Luther</rs></seg></line>
    <line>1. <seg><rs type="direct" ref="psn:Hilten">Johannes Hilten</rs></seg> (<seg><rs type="direct" ref="plc:Eisenach">Eiſe-</rs></seg></line>
    <!-- … -->
  </zone>
</surface>
```

--

![highlighted entities at the transcription view](img/c71r-highlighted-entities.png) <!-- .element: style="max-height:18em" -->

^Note: When we apply this to all entites on this page, we have to encode all
the text highlighted on this screenshot. Focusing on the entities
exclusively, we are about to create a tree-like structure…

--

<iframe height="650" width="650" src="examples/3.html"></iframe>

^Note: To turn this tree into a network, we have to remove the duplicates. In a
network we can have only a single representative for each “observation”.

--

<iframe height="650" width="650" src="examples/4.html"></iframe>

--

<!-- .slide: data-background-iframe="https://fontane-nb.dariah.eu/tei-conf/rtt/" -->

---

## Network Analysis

internet, formalism

---

## Outlook

The more the merrier<span class="fade-out">!</span>

No! <!-- .element: class="fragment" -->

--

Text sources needs to be accessible:

It is pretty easy to over-engineer a resource. It is much harder to reach out
for the communities requirements.
