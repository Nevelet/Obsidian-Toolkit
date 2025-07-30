---
tags:
  - categorie
cssclasses:
  - wide
  - cards
banner: "[[tom-hermans-9BoqXzEeQqM-unsplash.jpg]]"
---



## In lettura

```dataview
TABLE  WITHOUT ID 
	choice(contains(cover, "https"), ("![coverimg|100](" + cover + ")"), choice(cover, embed(link(cover, "100")), ![[book cover.png|100]])) as Cover,
	file.link AS Libri,
	"Pagine: " + pagine AS Pagine,
	"Pagine lette: " + pagine-lette AS "Pagine Lette",
	"Autore: " + autore AS Autori,
	"Anno: " + anno AS Anni,
	"Voto personale: " + voto-personale AS "Voto personale",
	    choice(pagine-lette and pagine, "<progress value='" + string((default(pagine-lette, 0) / default(pagine, 1)) * 100) + "' max='100'></progress>" + " " + round((default(pagine-lette, 0) / default(pagine, 1)) * 100) + "%", "No Data") AS "Progresso"

FROM #source

WHERE 
	contains(tipo, "Libro") AND
	contains(stato, "Attivo") AND 
	!contains(file.path,"Templates") 

```

## Da leggere

```dataview
TABLE  WITHOUT ID 
	choice(cover, ("![coverimg|100](" + cover + ")"), ![[book cover.png|100]]) as Cover,
	file.link AS Libri,
	"Pagine: " + pagine AS Pagine,
	"Pagine lette: " + pagine-lette AS "Pagine Lette",
	"Autore: " + autore AS Autori,
	"Anno: " + anno AS Anni,
	"Voto personale: " + voto-personale AS "Voto personale",
	    choice(pagine-lette and pagine, "<progress value='" + string((default(pagine-lette, 0) / default(pagine, 1)) * 100) + "' max='100'></progress>" + " " + round((default(pagine-lette, 0) / default(pagine, 1)) * 100) + "%", "No Data") AS "Progresso"

FROM #source

WHERE 
	contains(tipo, "Libro") AND
	contains(stato, "Leggere") AND 
	!contains(file.path,"Templates") 

```

## Letti

```dataview
TABLE  WITHOUT ID 
	choice(cover, ("![coverimg|100](" + cover + ")"), ![[book cover.png|100]]) as Cover,
	file.link AS Libri,
	"Pagine: " + pagine AS Pagine,
	"Pagine lette: " + pagine-lette AS "Pagine Lette",
	"Autore: " + autore AS Autori,
	"Anno: " + anno AS Anni,
	"Voto personale: " + voto-personale AS "Voto personale",
	    choice(pagine-lette and pagine, "<progress value='" + string((default(pagine-lette, 0) / default(pagine, 1)) * 100) + "' max='100'></progress>" + " " + round((default(pagine-lette, 0) / default(pagine, 1)) * 100) + "%", "No Data") AS "Progresso"

FROM #source

WHERE 
	contains(tipo, "Libro") AND
	contains(stato, "Letto") AND 
	!contains(file.path,"Templates") 

```

