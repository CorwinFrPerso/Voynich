# Plan expérimental

## Ordre des priorités

1. **Crib iconographique/documentaire**.
2. **Primitives robustes R0** uniquement.
3. **q / qo** et contraintes positionnelles.
4. **gallows / bench-gallows** comme familles structurées.
5. **formes longues / split gallows**.
6. seulement ensuite modèles vocaliques, morphographiques et linguistiques.

## Axe A : crib

### A1. Corpus d'herbiers

Construire un corpus de manuscrits XIVe-XVe siècles avec ordre des plantes préservé.

Pour chaque source :

- identifiant manuscrit ;
- date ;
- lieu/provenance ;
- folio ;
- nom de plante donné par le manuscrit ;
- image ;
- texte associé ;
- position dans la séquence.

### A2. Recherche de séquences

Mesurer deux scores :

```text
S_image = ressemblance grossière des illustrations
S_order = cohérence des voisins / ordre relatif
```

Puis :

```text
S_total = combinaison calibrée sur corpus négatif
```

Tester les séquences de 2 à 5 pages, avec gaps permis.

### A3. Validation prospective

Toute source découverte sur N pages doit prédire au moins une page non utilisée pour la découverte.

## Axe B : alphabet robuste

Ne pas analyser les micro-détails.

Features R0 :

- base `c/i/o/8/gallow/...` ;
- nombre de hampes ;
- boucle gauche oui/non ;
- boucle droite oui/non ;
- rail oui/non ;
- insertion dans un bench oui/non ;
- position début/milieu/fin ;
- espace traversé par une structure longue oui/non.

## Axe C : tests gallows

### C1. Paire f/p

Mesurer la distribution de `f` et `p`.

### C2. Paire k/t

Mesurer la distribution de `k` et `t`.

### C3. Test d'opérateur

Si boucle gauche = opérateur, alors la transformation contextuelle :

```text
f -> p
```

doit ressembler à :

```text
k -> t
```

### C4. Bench

Comparer gallows nus et gallows insérés dans un `c...c` relié par rail.

## Axe D : q / qo

Questions :

1. quel pourcentage de q est initial ?
2. combien sont suivis de o ?
3. quels suffixes suivent `qo` ?
4. q varie-t-il par Currier, section, scribe ?
5. les mots q ont-ils un rôle particulier en début de ligne/paragraphe ?

Modèles concurrents :

- q = lettre ;
- q = préfixe ;
- q = marqueur grammatical ;
- qo = macro indivisible ;
- q = opcode de reconstruction.

Comparer par vraisemblance et simplicité.

## Axe E : split gallows

Inventaire complet, puis tests :

- mêmes primitives que gallows normaux ?
- traverse un vrai espace de transcription ?
- chunks reliés ont-ils une propriété commune ?
- apparaissent-ils dans contextes de listes/recettes ?

## Axe F : modèle vocalique latent

À lancer uniquement après stabilisation du niveau graphique.

Comparer :

- M0 alphabet plat ;
- M1 alphabet featural ;
- M2 base consonantique + opérateur vocalique ;
- M3 syllabaire / morphogrammes.

Critères :

- perplexité tenue à l'écart ;
- BIC/AIC ;
- robustesse par folio/scribe ;
- prédiction hors échantillon.

## Axe G : langues candidates

Ne jamais optimiser uniquement sur une langue.

Corpus témoins minimum :

- latin médiéval médical ;
- Early New High German ;
- allemand dialectal pertinent ;
- italien médiéval/nord italien ;
- tchèque/allemand si provenance l'exige ;
- langues négatives de contrôle.

## Métriques générales

- fréquence ;
- position dans le groupe ;
- voisin gauche/droit ;
- mutual information ;
- Jensen-Shannon distance ;
- log-odds ;
- modèle hiérarchique par scribe/section ;
- perplexité held-out ;
- MDL : minimum description length.

## Critère de victoire

### Étape 1
Une source candidate prédit une séquence iconographique non utilisée pour la trouver.

### Étape 2
Le texte associé fournit un crib qui contraint fortement le système de transcription.

### Étape 3
Un petit nombre de règles graphiques explique plusieurs familles de glyphes.

### Étape 4
Ces règles permettent de prédire un texte non vu.

Aucun « mot reconnaissable » isolé ne compte comme victoire.