# flutter_application_4

# Temes Git
# Iniciar un repositori

```
git init -> inicialitza repositori local A la carpeta del S.O.
git add . registra al git els arxius a sincronitzar (excepte del git.ignore)
git commit -m "initial commit" (Al repositori local)
git remote ad origin http://...
git push -u origin main
```

# Pull, fetch, merge

`
Git pull = fetch origin/main (branca de seguimnt/upstream) + merge origin/main
`

# Clone

```
git clone http://  (etiqueta automàticament com origin)
    -> Descarrega totes les branques
    -> Estableix la branca local activa per defecte (main)
    -> Checkout de la brancaper defete a local
```

# Comprovar canvis

```
git log --oneline
Git diff branca_local branca_de_seguiment
```

# Resturar canvis

```
git reset --hard id_del_commit <-Si no s'ha fet push, no conserva els canvis
git revert  id_del_commit <-Si s'ha fet push i es vol conservarels canvis
git reset --hard id_commit;git push --force <- no conserva canvis al repo
```

# Afegir remots

```
git remote add origin http://....
git remote add origin2 http://....
```

# Veure els remots


`git remote-v`

# Establir upstream per defecte

```
git push -u origin main <-Primer commit a repositori verge
git branch -- set-upstream-to origin2/main
```

# Git ignore

```
git add . ignora els del .ignore
Per a treure arxius 'trackejats' fer:
git  rm --cached nombdelaxiu (con --cached no l'esborra del S.O)
i posar-los al git.ignore
```

# Patró a .gitignore
```
*.log      -> Ignora arxius de log all directorio raíz
**/logs  -> Ignora qualsevol directori que es digu logs a cualsevol nivell (ex., src/logs, tests/logs, logs).
**/*.log  -> Ignora qualsevol arxiu que acabi amb .log a qualsevol subdirectori (ex., app.log, data/output.log).
build/**  -> Ignora tots els arxius i subdirectoris dintre de la carpeta build/. Això és mes específic i no recursiu a nivell global, si no de build.
```

# Gestió ràpida de conflictes

```
git status
git checkout --ours nom_arxiu
git checkout --theirs nom_arxiu
```

# Gestió quirúrgica de conflictes

```
git status
git diff
editar els arxius en conflicte
Per a cada conflicte:
    Si vull el que es meu
        Em quedo amb el que hi ha entre:  <<<<<<< HEAD i =======
    Si vull el quehi ha al repositori
        Quedar-se amb el que hi ha entre:  ======= i >>>>>>> f12a3b4...
```

Portar un canvi d'altre repositori

```
git remote add origin2 http://....
git branch --set-upstream-to origin2/main (sólo cambia para el pull)
git checkout origin2/main README.md
git branch --set-upstream-to origin/main (sólo cambia para el pull)
git add README.md
git commit -m "el que sigui"
git push
```

Restaurar l'arxiu anterior

```
git checkout f3e020e README.md
add, commit, y push
```

Mostrar branques de seguiment

`git branch -r`

# Forks de [bemen3-0489-dam-prac-0488-ra3i4-flutter_empty](https://github.com/Bemen3M07/bemen3-0489-dam-prac-0488-ra3i4-flutter_empty)

| # | Repositori | URL |
|---|-----------|-----|
| 1 | Bemen3M07/prac-0488-ra3i4-aamalu25 | https://github.com/Bemen3M07/prac-0488-ra3i4-aamalu25 |
| 2 | Bemen3M07/prac-0488-ra3i4-ALDA24-Ali | https://github.com/Bemen3M07/prac-0488-ra3i4-ALDA24-Ali |
| 3 | Bemen3M07/prac-0488-ra3i4-dacaga24-cpu | https://github.com/Bemen3M07/prac-0488-ra3i4-dacaga24-cpu |
| 4 | Bemen3M07/prac-0488-ra3i4-damasa25-blip | https://github.com/Bemen3M07/prac-0488-ra3i4-damasa25-blip |
| 5 | Bemen3M07/prac-0488-ra3i4-darolo24-star | https://github.com/Bemen3M07/prac-0488-ra3i4-darolo24-star |
| 6 | Bemen3M07/prac-0488-ra3i4-dateni24-dot | https://github.com/Bemen3M07/prac-0488-ra3i4-dateni24-dot |
| 7 | Bemen3M07/prac-0488-ra3i4-Diego-bemen3 | https://github.com/Bemen3M07/prac-0488-ra3i4-Diego-bemen3 |
| 8 | Bemen3M07/prac-0488-ra3i4-EdimBatalla | https://github.com/Bemen3M07/prac-0488-ra3i4-EdimBatalla |
| 9 | Bemen3M07/prac-0488-ra3i4-gucaca23-coder | https://github.com/Bemen3M07/prac-0488-ra3i4-gucaca23-coder |
| 10 | Bemen3M07/prac-0488-ra3i4-keacma24-a11y | https://github.com/Bemen3M07/prac-0488-ra3i4-keacma24-a11y |
| 11 | Bemen3M07/prac-0488-ra3i4-macasa24-collab | https://github.com/Bemen3M07/prac-0488-ra3i4-macasa24-collab |
| 12 | Bemen3M07/prac-0488-ra3i4-mabi24-lang | https://github.com/Bemen3M07/prac-0488-ra3i4-mabi24-lang |
| 13 | Bemen3M07/prac-0488-ra3i4-nidaaghajz | https://github.com/Bemen3M07/prac-0488-ra3i4-nidaaghajz |
| 14 | Bemen3M07/prac-0488-ra3i4-niriga24-sudo | https://github.com/Bemen3M07/prac-0488-ra3i4-niriga24-sudo |
| 15 | Bemen3M07/prac-0488-ra3i4-no-data-no-plan | https://github.com/Bemen3M07/prac-0488-ra3i4-no-data-no-plan |
| 16 | Bemen3M07/prac-0488-ra3i4-POrtizDiaz | https://github.com/Bemen3M07/prac-0488-ra3i4-POrtizDiaz |
| 17 | Bemen3M07/prac-0488-ra3i4-ramonmascaro | https://github.com/Bemen3M07/prac-0488-ra3i4-ramonmascaro |
| 18 | Bemen3M07/prac-0488-ra3i4-rozy24bemen | https://github.com/Bemen3M07/prac-0488-ra3i4-rozy24bemen |
| 19 | Bemen3M07/prac-0488-ra3i4-saseju24-sys | https://github.com/Bemen3M07/prac-0488-ra3i4-saseju24-sys |
| 20 | Bemen3M07/prac-0488-ra3i4-TDano245 | https://github.com/Bemen3M07/prac-0488-ra3i4-TDano245 |
| 21 | Bemen3M07/prac-0488-ra3i4-Uxue24 | https://github.com/Bemen3M07/prac-0488-ra3i4-Uxue24 |
| 22 | Bemen3M07/prac-0488-ra3i4-viesna25-glitch | https://github.com/Bemen3M07/prac-0488-ra3i4-viesna25-glitch |
| 23 | mabi24-lang/prac-0488-ra3i4-no-data-no-plan | https://github.com/mabi24-lang/prac-0488-ra3i4-no-data-no-plan |
