---
title: Ricerca per Tag
---

```dataview
TABLE link(rows.file.name, rows.title) AS titolo
FROM #award
GROUP BY categories
SORT rows.title ASC
```

