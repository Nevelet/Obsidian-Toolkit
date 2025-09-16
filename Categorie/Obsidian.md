---
tags:
  - categorie
---


- [[Obsidian - Plugin di terze parti]]
- [[Obsidian - Plugin principali]]


**Guarda il corso completo su Obsidian 👇**
![video](https://youtu.be/FjkMf2KprnA?si=AdmX5VIsiI9naoXL)

[Video Tutorial OBSIDIAN (Playlist)](https://youtube.com/playlist?list=PLZBoOA4enayocyEuWybJw7RLkp749O6RH&si=ejk48jWH3lFTiwW-)


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
