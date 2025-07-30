---
tags:
  - categorie
---





```dataview
TABLE
	tags as Tags
FROM [[]] and !outgoing([[]])
WHERE !contains(file.path, "Templates")
SORT created desc
```
