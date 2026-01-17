---
title: "**Lezione 4**"
---

Argomenti trattati:
===

<!-- alignment: center -->

<!-- jump_to_middle -->

- Web Development
  - Come è composta una pagina web
  - Introduzione generale all HTML

<!-- end_slide -->

Come è composta una pagina web
===

Una pagina web è la base di un sito

È composta da 2 parti fondamentali:

- metadati e altre informazioni utili per la SEO (Search Engine Optimization)
- Contenuto effettivo della pagina

---

**metadati e altre informazioni utili per la SEO**:

I metadati sono informazioni che servono ai search engines (per esempio google) a indicizzare meglio il sito, quindi di posizionarlo il meglio possibile tra tutti gli altri siti del web

Molte di queste informazioni non sono visibili all'utente

Però alcune lo sono:

- titolo
- descrizione
- preview per i vari social
- favicon (immagine che sta vicino al titolo della pagina)

I metadati sono solo una parte della SEO: anche altri fattori influiscono sul posizionamento del sito:

- tempo di caricamento della pagina
- presenza di un titolo, descrizione (le keywords oggi contano molto meno rispetto al contenuto reale)
- qualità della pagina (contenuto, se il sito usa HTTPS e non HTTP, se il sito è abbastanza responsivo)
- struttura della pagina (se c'è solo un H1, la struttura generale degli headings)

**contenuto effettivo della pagina**:

Una pagina web è composta come un essere umano e proprio per questo è divisa in 3 parti:

- HTML che costituisce lo scheletro della pagina (è come lo scheletro)
- CSS che definisce lo stile (quindi come la pelle e i vari tratti somatici)
- JS che rende interattiva la pagina (come gli occhi e la bocca)

> è importante notare che una pagina web può esistere anche senza CSS o JavaScript, o senza entrambi

<!-- end_slide -->

Introduzione generale all HTML
===

HTML sta per HyperText Markup Language, ed è il linguaggio che dà la struttura alla pagina web

Un documento HTML è composto come un albero, quindi ha vari livelli:

- html
  - head (la parte che contiene tutti i meta tag, altre informazioni utili al browser, come il collegamento ai file CSS e JavaScript):
    - charset (`<meta charset="UTF-8" />`)
    - titolo (`<title>...</title>`)
    - descrizione (`<meta name="description" content="..." />`)
    - altri metadati (`<meta name="..." content="..." />`)
    - link a CSS/JS esterni oppure per mettere il favicon (`<link rel="..." href="..." />`)
    - stili in-document (`<style>...</style>`)
    - scripts (`<script>...</script>`), ma spesso vengono messi nel body
    - setting del viewport (`<meta name="viewport" content="width=device-width, initial-scale=1.0">`), questo è utile per rendere il sito responsivo
  - body (quello che contiene il contenuto che l'utente vede e tipicamente contiene):
    - header
    - main
    - footer

<!-- end_slide -->

Il tag
===

L'elemento fondamentale dell HTML è il tag

Ci sono 2 tipi di tag:

- quelli che si devono chiudere (`<h1>...</h1>`, `<p>...</p>`)
- quelli che non si chiudono (detti _void elements_) (`<br />`, `<img ... />`, `<hr />`, `<meta ... />`), la / non è obbligatoria, ma la maggior parte dei formatters la mette di default

Ogni tag ha la stessa struttura:

- parentesi acute, usate per differenziare un tag da un testo normale
- nome del tag, messo tra le parentesi acute
- attributi che sono composti anche loro da:
  - nome
  - contenuto, generalmente messo tra virgolette e prima di esse bisogna mettere un =
  - un tag può contenere più di un attributo, tutti staccati da uno spazio
  - ci sono anche attributi che non hanno bisogno del contenuto
- contenuto (solo se il tag si deve chiudere)
- tag di chiusura se chiude ed è composto solo dal nome con una / prima del nome

**Esempio**:

``` html
<p class="...">Questo è un paragrafo</p>
 ^       ^              ^             ^
nome   attributo      contenuto     tag di chiusura
```

**Altro esempio**:

```html
<img src="..." alt="..." />
  ^     ^           ^
nome  attributo   altro attributo
```

---

Anche se in genere possiamo mettere quanti tag vogliamo, ci sono delle regole da rispettare (non sempre obbligatorie)

- mettere sempre un h1 per pagina, **mai più di 1**, metterne più di uno funziona, ma non è consigliato
- dividere la pagina, quando possibile, in **header**, **main** e **footer**
- chiudere **sempre** tutti i tag che lo richiedono
- mettere **sempre** i tag giusti in base al loro scopo (mai mettere un h2 per un paragrafo per esempio)
- ogni tag può ne può contenere un altro, però è meglio metterli in modo sensato (per esempio non ha senso mettere un `<h1></h1>` dentro un `<p></p>`, oppure un `<div></div>` dentro `<span></span>`)

<!-- end_slide -->

I tag più importanti e usati
===

- i vari headings, usati per i titoli, se il numero è più alto ha meno importanza semantica (di solito viene mostrato con una dimensione minore):
  - `<h1>...</h1>`
  - `<h2>...</h2>`
  - `<h3>...</h3>`
  - `<h4>...</h4>`
  - `<h5>...</h5>`
  - `<h6>...</h6>`
- paragrafo:
  - `<p>...</p>`
- link:
  - `<a href="...">...</a>`
- immagini:
  - `<img src="..." alt="..." />`, `alt="..."` è importante per l'accessibilità e la SEO, e serve a mostrare un testo quando l'immagine non si carica
- contenitori:
  - contenitore generico, in genere usato per blocchi:
    - `<div>...</div>`
  - contenitore per il testo, in genere usato per applicare stili su una porzione di testo:
    - `<span>...</span>`
  - altri contenitori, in genere con uno scopo ben preciso:
    - `<header>...</header>`, usato per creare l header della pagina
    - `<main>...</main>`, usato per creare il contenuto principale della pagina
    - `<footer>...</footer>`, usato per creare il footer della pagina
    - `<nav>...</nav>`, usato per creare una navigation bar, in genere si trova dentro l header
    - `<section>...</section>`, sezione tematica della pagina
    - `<aside>...</aside>`, contenuto laterale / secondario
    - `<article>...</article>`, come dice il nome è fatto per gli articoli di un blog per esempio
    - `<address>...</address>`, usato per le informazioni di contatto dell'autore/proprietario della pagina
  - c'è da notare una cosa importante, questi tag non fanno fondamentalmente nulla, però vengono usati per la semantica della pagina e vengono modificati tramite CSS
- liste:
  - `<ul>...</ul>`, liste non ordinate
  - `<ol>...</ol>`, liste ordinate
  - `<li>...</li>`, sta per list items e va dentro la lista
- tabelle:
  - `<table>...</table>`, il tag che definisce una tabella
  - una tabella è divisa in 3 parti:
    - `<thead>...</thead>`, contiene l header della tabella (in genere la prima riga)
    - `<tbody>...</tbody>`, contiene il contenuto effettivo della tabella
    - `<tfoot>...</tfoot>`, contiene il footer della tabella
  - tutte quante le parte sono divise allo stesso modo:
    - `<tr>...</tr>`, per definire una riga (sta per table row)
    - `<td>...</td>`, per definire una cella della tabella (sta per table data), ogni cella fa parte di una colonna
    - però per l header della tabella è meglio usare `<th></th>` invece di `<td></td>` (sta per table heading)

<!-- end_slide -->

I tag più importanti e usati
===

- vari tag per cambiare la tematica:
  - `<b>...</b>`, per rendere una parte di testo in grassetto, senza dargli così tanta importanza
  - `<strong>...</strong>`, per dare importanza ad una parte di testo, in genere rende il testo in grassetto
  - `<i>...</i>`, per rendere una parte di testo con una voce o mood diverso, in genere rende il testo in corsivo
  - `<em>...</em>`, per enfatizzare una parte di testo, in genere rende il testo in corsivo
- forms:
  - `<form>...</form>`, per definire il form
  - `<input>...</input>`, campo dove l’utente scrive o interagisce. Tipo: testo, password, checkbox, radio, submit, ecc
  - `<label>...</label>`, testo descrittivo collegato a un `<input>`. È utile perché cliccando sul testo si attiva il campo
- commenti:
  - `<!-- ... -->`, i commenti sono sezioni che non vengono mostrati, servono in genere per disabilitare una parte di codice oppure per fare commenti sul codice

<!-- end_slide -->

Esempio di una pagina html:
===

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Titolo della pagina</title>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="icon" type="image/svg+xml" href="favicon.svg" />
    <link rel="stylesheet" href="file-css.css" />
  </head>
  <body>
    <header id="header">
      <h1 id="titolo-header">
        Titolo nel header
      </h1>
      <nav id="navigation-bar">
        <ul id="lista">
          <li class="link-navbar">
            <a href="link-alla-pagina.html">
              Home page
            </a>
          </li>
          <li class="link-navbar">
            <a href="link-alla-pagina.html">
              Altra Pagina
            </a>
          </li>
        </ul>
      </nav>
    </header>

    <main id="main">
      <section id="sezione">
        <p id="paragrafo">sezione della pagina</p>
      </section>
    </main>

    <footer id="footer">
      <span id="contenuto-footer">Footer della pagina</span>
    </footer>
  </body>
</html>
```
Quando faremo il CSS parleremo di ID e classi
