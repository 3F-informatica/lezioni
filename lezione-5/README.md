---
title: "**Lezione 5**"
---

Argomenti trattati
===

<!-- alignment: center -->

<!-- jump_to_middle -->

- Introduzione al CSS

<!-- end_slide -->

Introduzione al CSS
===

Il CSS (Cascading Style Sheet) è un linguaggio a cascata che serve per dare degli stili nel HTML

Si chiama _cascading_ perché più regole possono applicarsi allo stesso elemento,
e il browser decide quale usare in base a priorità, specificità e ordine,
sovrascrivendo le altre solo se modificano la stessa proprietà.

---

## Tabella sulle priorità

Ogni selettore in CSS ha una posizione gerarchica precisa, e ogni selettore ha un "peso" diverso

<!-- alignment: center -->

| Selettore        | Esempio                     | Priorità          | Peso  |
|------------------|-----------------------------|-------------------|-------|
| Inline           | `<h1 style="color: red">` | priorità più alta | - (fuori dalla specificità) |
| Selettori con ID | `#titolo`                   | secondo           | 1-0-0 |
| Classi, selettore di attributo e pseudo-classi | `.titoli`, `[type="titolo"]`, `:hover` | terzo | 0-1-0 |
| Elementi e pseudo-elementi | `h1`, `::before`, `::after` | priorità bassa | 0-0-1 |
| Selettore universale e `:where()` | `*`, `where()` | No priorità | 0-0-0 |

<!-- alignment: left -->

La dichiarazione con il peso più alto che modifica la stessa proprietà viene applicata all'elemento

```html
<html>
  <head>
    <style>
      #demo {  /* peso: 1-0-0 */
        color: blue;
      }
      p#demo { /* peso: 1-0-1, ha il peso più alto, quindi viene applicato questo */
        color: orange;
      }
      .test {  /* peso: 0-1-0 */
        color: green;
      }
      p.test { /* peso: 0-1-1 */
        color: green;
      }
      p {      /* peso: 0-0-1 */
        color: red;
      }
    </style>
  </head>
  <body>
    <p id="demo" class="test">Hello World!</p>
  </body>
</html>
```

<!-- end_slide -->

Introduzione al CSS
===

Se 2 selettori modificano lo stesso elemento e hanno lo stesso peso l'ultimo stile viene applicato:

```html
<html>
  <head>
    <style>
      p { /* peso: 0-0-1 */
        color: red;
      }

      p { /* peso: 0-0-1, questo viene applicato perché è l'ultimo stile */
        color: green;
      }
    </style>
  </head>
  <body>
    <p>Hello World!</p>
  </body>
</html>
```

C'è anche un altro selettore che sovrascrive tutto, `!important`, forza una regola a vincere sulla cascata, ma andrebbe evitato perché rompe la prevedibilità del CSS

---

Ci sono 3 metodi per inserire CSS nel codice:

- Inline
  - `<h1 style="...">`
- Interno
  - `<style>...</style>`, questo va dentro la `<head></head>`
- Esterno
  - Questo è il metodo preferito per mettere il CSS, perché separa l HTML dal CSS: `<link rel="stylesheet" href="percorso/stile.css" />`

Anche loro hanno delle priorità, l'inline ha la più alta, invece per quello esterno e interno dipende da come vengono scritti nella head:

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

```html
<head>
  <style>
    ...
  </style>
  <link ... />
</head>
```


<!-- alignment: center -->
Qua il CSS esterno ha più priorità

<!-- column: 1 -->

```html
<head>
  <link ... />
  <style>
    ...
  </style>
</head>
```

<!-- alignment: center -->

Qua il CSS interno ha più priorità

<!-- reset_layout -->

<!-- end_slide -->

Selettori
===

I selettori vengono usati per selezionare l'elemento HTML dove si vuole applicare gli stili

Ci sono 5 categorie di selettori:

- Selettori semplici (seleziona elementi in base a nome, classe e ID)
- Selettori combinati (seleziona elementi in base ad una specifica relazione tra loro)
- Selettori di pseudo-classi (selezione gli stili in base ad uno stato specifico)
- Selettori di pseudo-elementi (seleziona una parte specifica di un elemento)
- Selettori di attributi (seleziona gli elementi in base ad attributi o valori di attributi)

---

**Selettore di un elemento**:

Seleziona un elemento in base al nome

```css
p {
  text-align: center;
  color: red;
}
```

**Selettore di ID**:

Seleziona un elemento in base all ID

L'ID è unico, e lo può avere solo un elemento, e quell'elemento può avere solo un ID

Per selezionarlo nel CSS si mette un `#` e poi il nome dell'ID

```css
#paragrafo1 {
  text-align: center;
  color: red;
}
```
> [!IMPORTANT]
> Un ID non può iniziare con un numero!

<!-- end_slide -->

Selettori
===

**Selettore di classe**:

Seleziona gli elementi con una classe

La classe a differenza dell'ID può essere applicata a quanti elementi vogliamo e un elemento può averne più di una

Per selezionare una classe in CSS si scrive un `.` e poi il nome della classe

```css
.paragrafo {
  text-align: center;
  color: red;
}
```

Si può anche specificare quale elemento viene affetto da una classe

```css
p.paragrafo {
  text-align: center;
  color: red;
}
```

> [!IMPORTANT]
> Come gli ID, le classi non possono iniziare con un numero

**Selettore universale**:

Il selettore universale (`*`) seleziona tutti gli elementi di una pagina

```css
* {
  text-align: center;
  color: blue;
}
```

<!-- end_slide -->

Selettori
===

I selettori raggruppati servono per applicare a più elementi lo stesso stile

Quindi invece di scrivere:

```css
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

Si possono separare i nomi degli elementi con una virgola:

```css
h1, h2, p {
  text-align: center;
  color: red;
}

```

<!-- end_slide -->

Box model
===

Il box model è una cosa fondamentale nel CSS, ed è una "scatola" che avvolge ogni elemento dell HTML

Con un immagine è molto più semplice da capire che scritto:

![image:width:50%](./assets/box_model.png)

<!-- end_slide -->

Com'è composto uno stile di CSS
===

Tutti gli stili CSS hanno lo stesso formato:

```
<selettore> {
  <proprietà>: <valore>;
  <proprietà>: <valore>;
  ...
}
```

Dei selettori ne abbiamo già parlato, mentre proprietà e valori li vediamo ora

Di proprietà ce ne sono tantissime, e i valori cambiano in base alla proprietà

Ecco le proprietà più comuni:

- Font e testo:
  - `color`
  - `font-size`
  - `font-family`
  - `font-weight`, "peso" del font (più è alto più è in grassetto)
  - `font-style`, stile del font, se normale, in corsivo oppure obliquo
  - `line-height`, altezza delle righe
  - `text-align`, come allineare il testo (destra, sinistra, centro)
  - `text-decoration`, decorazione del testo (sottolinea, linea in mezzo al testo, oppure sopra al testo)
  - `text-transform`, controlla come capitalizzare il testo (se mettere tutto in maiuscolo, minuscolo oppure ogni prima lettera di una parola in maiuscolo)
  - `letter-spacing`
  - `word-spacing`
- Box model:
  - `width`
  - `height`
  - `min-width`
  - `max-width`
  - `min-height`
  - `max-height`
  - `margin`
  - `padding`
  - `border`
  - `box-sizing`, descrive come l'altezza e larghezza di un elemento viene calcolata, se bisogna contare padding e bordo, oppure no
- Colori e sfondi:
  - `background`
  - `background-color`
  - `background-image`
  - `background-size`
  - `background-position`
  - `background-repeat`
  - `opacity`

<!-- end_slide -->

Esempio di una pagina fatta con CSS
===

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      * {
        padding: 0px;
        margin: 0px;
        box-sizing: border-box;
      }

      body {
        background-color: #181616;
      }

      #titolo {
        color: #76946A;
        font-size: 32px;
        font-weight: bold;
        text-transform: uppercase;
      }

      .paragrafo {
        margin-top: 8px;
        color: #ffffff;
        font-size: 16px;
      }

      #link {
        text-decoration: none;
      }

      #link:hover {
        text-decoration: underline;
      }
    </style>
  </head>
  <body>
    <h1 id="titolo">titolo</h1>
    <p class="paragrafo">testo</p>
    <p class="paragrafo">testo</p>
    <a id="link" href="..." style="color: cyan">Link</a>
  </body>
</html>
```

Qua ho usato gli ID, però in genere è sempre meglio usare le classi
