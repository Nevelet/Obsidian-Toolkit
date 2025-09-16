---
tags:
  - categorie
---





```base
filters:
  and:
    - '!file.path.contains("Templates")'
views:
  - type: table
    name: Backlinks
    filters:
      and:
        - file.hasLink(this.file)
        - "!file.backlinks.contains(this)"
    order:
      - file.name
      - file.tags
      - creazione
    columnSize:
      file.name: 329

```
