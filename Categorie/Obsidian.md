---
tags:
  - categorie
---


- [[Obsidian - Plugin di terze parti]]
- [[Obsidian - Plugin principali]]


**Guarda il corso completo su Obsidian 👇**
![video](https://youtu.be/FjkMf2KprnA?si=AdmX5VIsiI9naoXL)

[Video Tutorial OBSIDIAN (Playlist)](https://youtube.com/playlist?list=PLZBoOA4enayocyEuWybJw7RLkp749O6RH&si=ejk48jWH3lFTiwW-)


```dataview
TABLE
	tags as Tags
FROM [[]] and !outgoing([[]])
WHERE !contains(file.path, "templates")
SORT created desc
```
