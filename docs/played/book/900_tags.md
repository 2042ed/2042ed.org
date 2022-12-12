---
title: Indice per Tag
slug: tags
summary: per trovare un gioco in base a delle parole chiave
date: 2021-04-01
type: book
tags: [PlayED]
weight: 900
updated: 2022-03-22
---
# Indice per Tag
In giro per il libro hai visto vari tags, per tipologia di gioco o tema.
Potrebbe essere utile questo indice per trovare il gioco che fa per te!

Queste icone rappresentano:

- 🧠 mentale / intellettuale / logico
- 💭 ideazione / pensiero laterale
- 📜 memoria e gestione del passato
- 🔢 matematica
- 🧡 emotivo / empatia / sentimenti
- 🗣 parole e comunicazione
- 💡 immaginazione / astrazione
- 💪 motorio / destrezza
- 👀 percezione / visione
- 🛠 progettazione e costruzione
- 🎲 casualità
- 🎓 educativo
- 🏆 nostro preferito


### #App

```dataview
LIST title
FROM #App
WHERE file.name != this.file.name
SORT title
```
