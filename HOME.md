---
banner: "[[leone-venter-VieM9BdZKFo-unsplash.jpg]]"
cssclasses:
  - wide
---


---
> [!multi-column]
>
>> ### **Vault**
>> Nota del giorno: `= link(dateformat(date(today), "yyyy-MM-dd"))`
>> Note vault: `$= dv.pages().length`
>> Note create oggi: `$= const today = window.moment().startOf("day"); dv.pages().filter(p => p.file.ctime >= today).sort(p => p.file.ctime, 'asc').length `
>
>> ### **Note rapide**
>> [[Progetti]]
>> [[Libri]]
>> [[Obsidian]]
>> [[README]]

---
> [!multi-column]
>
>> ### **Ultime 5 note create**
>> `$= dv.list(dv.pages().sort(f => f.file.ctime.ts, "desc").limit(5).file.link)`
>
>> ### **Ultime 5 note modificate**
>> `$= dv.list(dv.pages().sort(f => f.file.mtime.ts, "desc").limit(5).file.link)`
>
>> ### **Note create oggi**
>> `$= const today = window.moment().startOf("day"); dv.list(dv.pages().filter(p => p.file.ctime >= today).sort(p => p.file.ctime, 'asc').limit(20).file.link) `
>




