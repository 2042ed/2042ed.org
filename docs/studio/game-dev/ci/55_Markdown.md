---
title: Markdown
date: 2022-12-23
updated: 2023-02-03
type: book
weight: 55
toc: true
draft: false
---
# Markdown

![](../../../assets/img/gamedev/img-ci/markdown_logo.webp)

Il formato Markdown è stato creato in contrapposizione al _markup_ dell'HTML.
Qui la base è testo semplice con pochissime convenzioni che permettono al contenuto di essere poi convertito nei formati più utili (html, doc, pdf, ePub) garantendo un versioning perfetto e una preservazione e portabilità ottimali

GitHub ha determinato massicciamente l'adozione dello standard Markdown per la documentazione e la scrittura in generale e ormai moltissimi siti vengono generati con Static Site Generators (vedi Jekyll o Hugo) a partire da contenuti scritti in Markdown, e la maggior parte degli editor di testo lo supportano nativamente.

## Playground
guadare il codice di questa pagina per capire

note: GitHub ha una sua versione di MarkDown: <https://github.github.com/gfm/>

### Heading 3

Text under Heading 3

#### Heading 4

Text under Heading 4

##### Heading 5

Text under Heading 5

### Emphasis

*Emphasis*, aka italics, with *asterisks* or _underscores_.  
Strong emphasis, aka bold, with **asterisks** or __underscores__.  
Combined emphasis with **asterisks and _underscores_**.  
Strikethrough uses two tildes. ~~Scratch this.~~  
Highlights ==this part of text.==
And `keywords`.  

### Emojis
🤣
[🤣](https://stefanocecere.com) 

### Links

**External links**  
- ![nome del link](https://www.sito.com)
- [www.google.com](https://www.google.com)  
- [www.google.com with title](https://www.google.com "Google's Homepage")   
URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com> and sometimes
example.com (but not on Github, for example).

**Internal links**  
This links to the [Introduction](10_Introduzione.md)

### Code

We can highlight a `single keyword` or code blocks:

```
10 PRINT "generic code block"
20 GOTO 10
```

```csharp
class myClasse {
}
```

```markdown
here we can write code.  
or **strong** test
```

### Definitions

Parola da definire
:  è una cosa che si fa e non si dice

Una seconda parola
:  qui definiamo un'altro termine

### List

1. First ordered list item
2. Another item
3. Another item
4. Another item
   - Unordered sub-list.
   - Unordered sub-list.
   - Unordered sub-list.
5. Actual numbers don't matter, just that it's a number
     1. Ordered sub-list
     2. Ordered sub-list
     3. Ordered sub-list
6. the last item.
  You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

To have a line break without a paragraph, you will need to use two trailing spaces.  
Note that this line is separate, but within the same paragraph.  
(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

### Images

Save your image (jpg or png format only) to `img/` and insert it like this:

![Figure 1 caption text](../../../assets/img/gamedev/img-ci/image.webp)

### Tables

We can have nice tables.  
Colons can be used to align columns.  


| colonna | colonna 2 |
| --- | --- |
| valore | calore 2|



| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Table: Table captions are done like this.

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

### Blockquotes

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

### Maths

$$
y = -2.2x + 0.5
$$

$a+b= \frac{c}{c}$
$$a+b= \frac{c}{c}$$

$\lim{n \to \infty} x^{n+9}$
$$\lim{n \to \infty} x^{n+9}$$

$$\begin{aligned}
  a+b &= c           \
  b &= c - a         \
  1 &= \frac{b}{c-a} \
\end{aligned}$$

### Footnotes

Footnotes are best placed right after the paragraph first used.[^footnote]

[^footnote]: But you can also put them at the end of the document.

If you want to use endnotes instead turn them on in document options.

### Comments

We can have comments in the text

<!-- Comments are not shown in the final PDF -->

## Approfondimenti

- dal creatore di Markdown: <https://daringfireball.net/projects/markdown/syntax>
- Jekyll è il rendering engine delle GitHub pages: <https://jekyllrb.com>
- corso markdown: <https://lab.github.com/githubtraining/communicating-using-markdown>
