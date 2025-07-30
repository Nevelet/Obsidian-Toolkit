---
banner: "[[markus-winkler-Q2J2qQsoYH8-unsplash.jpg]]"
tags:
  - categorie
cssclasses:
  - wide
  - no-wrap
---
[[HOME]]

---
## ▶ Attivi

```dataview
TABLE WITHOUT ID
    file.link AS Progetti,
	priorità AS Priorità,
    scadenza AS Scadenza,
    categorie AS Categorie

    
FROM #project

WHERE 
	contains(stato, "Attivo") AND
	!contains(file.path, "Templates")



SORT choice(scadenza, scadenza, "") ASC
// SORT choice(!scadenza, scadenza, scadenza) DESC
SORT stato DESC
SORT priorità DESC

LIMIT 20

```


## ⌚ In attesa

```dataview
TABLE WITHOUT ID
    file.link AS Progetti,
	priorità AS Priorità,
    scadenza AS Scadenza,
    categorie AS Categorie

    
FROM #project

WHERE 
	contains(stato, "Attesa") AND
	!contains(file.path, "Templates")



SORT choice(scadenza, scadenza, "") ASC
// SORT choice(!scadenza, scadenza, scadenza) DESC
SORT stato DESC
SORT priorità DESC

LIMIT 20

```

## 🗑 Abbandonati

```dataview
TABLE WITHOUT ID
    file.link AS Progetti,
	priorità AS Priorità,
    scadenza AS Scadenza,
    categorie AS Categorie

    
FROM #project

WHERE 
	contains(stato, "Abbandonato") AND
	!contains(file.path, "Templates")



SORT choice(scadenza, scadenza, "") ASC
// SORT choice(!scadenza, scadenza, scadenza) DESC
SORT stato DESC
SORT priorità DESC

LIMIT 20

```

## ✅ Completati

```dataview
TABLE WITHOUT ID
    file.link AS Progetti,
	priorità AS Priorità,
    scadenza AS Scadenza,
    categorie AS Categorie

    
FROM #project

WHERE 
	contains(stato, "Completato") AND
	!contains(file.path, "Templates")



SORT choice(scadenza, scadenza, "") ASC
// SORT choice(!scadenza, scadenza, scadenza) DESC
SORT stato DESC
SORT priorità DESC

LIMIT 20

```


