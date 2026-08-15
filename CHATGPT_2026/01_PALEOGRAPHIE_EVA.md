# Décomposition paléographique EVA

Cette table est une **hypothèse de travail proposée par Guillaume**, à conserver séparément d'EVA, v101 et de toute interprétation linguistique.

| EVA | Lecture paléographique de travail |
|---|---|
| a | `c + i` agglutinés |
| b | `c` + boucle ouverte montant du bas vers le haut |
| c | `c` avec rail partant vers la droite depuis le haut |
| d | forme de chiffre `8` |
| e | `c` |
| f | gallow : hampe haute + bouclette droite |
| g | probablement `d` avec trait inférieur plus long |
| h | `c` avec rail sur la tête arrivant de gauche |
| i | trait oblique de type `i` |
| j | proche d'un `8/d` partant d'un `i`, éventuellement `m` très serré |
| k | gallow à deux hampes reliées + bouclette droite ; parent de `f` avec seconde hampe descendant jusqu'en bas |
| l | `i` avec boucle traversante ; probablement glyphe propre |
| m | `i` + bouclette droite, composant semblable à celui de `f` |
| n | `i` + boucle montante depuis le bas |
| o | `o`, forme relativement neutre |
| p | `f` + boucle en haut à gauche |
| q | forme proche de `4` |
| r | `i` + boucle montante partant presque du haut |
| s | forme artificielle dans EVA ; souvent liée à `e/c + rail + ajout supérieur` ; le `s` de `sh` ne doit pas être assimilé naïvement au `s` autonome |
| t | `k` + même boucle gauche que `p = f + boucle gauche` |
| u | `e + n` agglutinés |
| v | glyphe probablement propre sur base de trait `i`, sorte de v inversé |
| x | proche de `v` avec une forme de t sur la tête |
| y | forme de g cursif / 9 descendu |
| z | possible gallow `k` miniaturisé ou `m` mal formé |

## Relations prioritaires

### Famille c / rail

- `e ≈ c`
- `ch` doit être observé visuellement comme quelque chose de proche de `c + c` reliés par un rail sur leur tête.
- `sh` paraît partager le même squelette avec une marque/bouclette supplémentaire.
- Les chaînes ASCII EVA ne doivent jamais être prises comme segmentation linguistique.

### Famille gallows

Hypothèse structurale forte :

- `p = f + boucle gauche`
- `t = k + boucle gauche`
- `k` est structurellement apparenté à `f` par ajout/extension d'une seconde hampe.

Cela suggère une combinatoire de traits plutôt qu'un alphabet plat.

## Discipline de résolution

### R0 : invariants robustes
À conserver automatiquement : seconde hampe, boucle clairement présente, rail, classe générale `o/c/i/gallow`, position dans le groupe.

### R1 : variantes potentiellement fonctionnelles
À conserver seulement si répétées : boucle ouverte/fermée, queue systématiquement haute/basse, insertion stable d'un élément sous un rail.

### R2 : bruit scribal
À ignorer par défaut : angle fin, longueur exacte, contact imparfait, tremblement, épaisseur, courbure locale.

**Règle : coarse first, fine only when forced.**

## Point de désaccord utile avec d'autres décompositions

Les cas `a`, `g`, `j`, `z` sont particulièrement informatifs car plusieurs segmentations sont plausibles. Ils ne doivent pas être tranchés visuellement seuls : géométrie robuste + distribution + variantes intermédiaires doivent décider.