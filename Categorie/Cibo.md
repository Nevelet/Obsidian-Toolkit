---
tags:
  - categorie
---



```dataview
TABLE
FROM [[]] and !outgoing([[]])
WHERE !contains(file.path, "templates")
SORT created desc
```
