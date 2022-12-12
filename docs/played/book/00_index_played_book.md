---
title: PlayED - il libro
summary: il libro di questo progetto
date: 2020-12-14
type: book
weight: 0
updated: 2022-03-22
---
# PlayED - il libro
```dataview
LIST WITHOUT ID
link(file.name, title)
FROM "PlayED/book"
WHERE file.name != this.file.name
sort number(split(file.name,"_")[0])
```
