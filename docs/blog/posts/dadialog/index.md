---
title: Dialoghi con Papà
date: 2023-10-20
updated: 2024-03-19
tags: []
categories: []
authors:
  - stefano
---
# Dialoghi con Papà
una serie di dialoghi nel corso degli anni

```dataview
list from "docs/studio/dialoghi"
SORT rows.title ASC
```

```dataview
TABLE link(rows.file.name, rows.title) AS titolo
FROM "docs/studio/dialoghi" 
GROUP by categories
SORT rows.title ASC
```

