# Stratégie CRIB FIRST

## Pourquoi changer de stratégie

L'espace des possibilités est trop grand. Une recherche libre sur les glyphes, langues, substitutions et opérateurs peut produire indéfiniment de bonnes et de fausses pistes.

Décision : **ne plus attaquer prioritairement le cipher de face**.

Objectif : retrouver une source, un texte parallèle ou une séquence documentaire suffisamment contrainte pour fournir un crib.

## Inversion du problème

Au lieu de :

```text
Voynich -> déchiffrement -> sens -> source
```

chercher :

```text
image/structure Voynich -> source documentaire apparentée -> texte associé -> crib -> système Voynich
```

## Terrain prioritaire : Herbal A

Pourquoi :

- grand nombre de pages illustrées ;
- traditions médiévales d'herbiers avec ordre de plantes relativement stable ;
- une identification isolée de plante est faible ;
- une **séquence de plantes consécutives** est beaucoup plus discriminante.

### Règle

Ne jamais considérer :

```text
f9v ressemble à Viola
```

comme un crib.

Chercher plutôt :

```text
Voynich A -> source plante 37
Voynich B -> source plante 38
Voynich C -> source plante 39
Voynich D -> source plante 40
```

Si l'ordre est conservé, le texte de 37-40 devient un vrai candidat crib.

## Algorithme de chasse au crib iconographique

Pour chaque herbier candidat :

1. récupérer l'ordre complet des plantes ;
2. encoder chaque illustration par caractéristiques grossières :
   - architecture racine ;
   - nombre/forme générale des feuilles ;
   - disposition foliaire ;
   - architecture florale ;
   - symétrie ;
   - silhouette globale ;
3. ne pas rechercher seulement une similarité image-image ;
4. ajouter la similarité des voisins `n-2, n-1, n, n+1, n+2` ;
5. scorer les séquences de longueur 2, 3, 4, 5 ;
6. estimer la probabilité d'obtenir un score comparable par permutation aléatoire de l'ordre des plantes ;
7. ne retenir que les séquences très improbables sous le hasard ;
8. récupérer alors le texte exact associé aux plantes correspondantes.

## Second niveau : structure textuelle

Une source candidate doit ensuite être comparée au Voynich sans traduction directe.

Comparer :

- nombre de paragraphes ;
- longueur relative des entrées ;
- formules récurrentes ;
- titres éventuels ;
- fréquence de quantités ;
- répétitions lexicales ;
- position des mots similaires ;
- motifs de début/fin d'entrée.

Le bon crib doit produire des **contraintes avant même de connaître le code**.

## Autres terrains de crib

### Astro-médecine

Chercher des textes contemporains comprenant :

- signes zodiacaux ;
- parties du corps ;
- jours/heures ;
- saignée ;
- moments favorables/défavorables ;
- régimes de santé ;
- peu ou pas de mathématiques avancées.

L'objectif n'est pas de comparer des mots, mais les séquences de rubriques et de contenus attendus.

### Balnéologie

La section balnéologique peut être plus discriminante que l'herbier si elle dérive d'une tradition précise :

- thermes ;
- propriétés des eaux ;
- parties du corps ;
- indications thérapeutiques ;
- ordre des bains ou sources.

Chercher des traités du XIVe-XVe siècle avec séries d'illustrations ou organisation comparable.

### Recettes / pharmacopée

Les sections de petits paragraphes peuvent contenir des formules très stables :

- Recipe ;
- ana / de chaque ;
- poids ;
- préparation ;
- application ;
- indication.

Une structure récurrente identique dans une source connue peut devenir un crib même sans iconographie.

## Crib multi-signal

Un crib devient sérieux lorsqu'au moins trois signaux convergent :

1. **iconographie** : séquence d'images correspondante ;
2. **ordre** : mêmes voisins ou même structure de chapitres ;
3. **structure textuelle** : longueurs/répétitions compatibles ;
4. **chronologie/géographie** : source disponible vers 1400-1450 ;
5. **vocabulaire attendu** : latin médical / vernaculaire compatible.

## Règle de prédiction

La validation doit être prospective.

Exemple :

1. utiliser trois pages pour identifier une source candidate ;
2. cacher la quatrième page Voynich ;
3. prédire quelle illustration/source devrait suivre ;
4. seulement ensuite comparer.

Si la source ne prédit pas les pages suivantes, elle est rejetée.

## Approche algorithmique disruptive

### 1. Recherche séquentielle plutôt que reconnaissance d'image

Une plante médiévale peut être très stylisée. L'ordre des plantes est souvent plus informatif que la ressemblance brute.

### 2. Embeddings multimodaux comme générateur de candidats, jamais comme juge

Utiliser la vision moderne pour produire les 20 candidats les plus proches, puis scorer l'ordre et la structure documentaire.

### 3. Alignement de séquences tolérant les pertes

Les cahiers peuvent avoir été déplacés, des pages perdues ou des entrées omises.

Utiliser des algorithmes de type :

- dynamic time warping ;
- Smith-Waterman local ;
- Hidden Markov Model ;
- recherche de sous-séquences avec gaps.

### 4. Test contre corpus négatif

Tout score doit être comparé à des centaines de manuscrits sans rapport. Sans cela, une ressemblance visuelle n'a aucune valeur.

### 5. Bayesian update

Chaque signal doit modifier explicitement la probabilité d'une source candidate :

```text
P(source | image, ordre, texte, date, géographie)
```

Cela force à ne pas tomber amoureux d'une seule belle correspondance.

## Critère de succès

Premier vrai succès : trouver une séquence documentaire dont la correspondance au Voynich est suffisamment forte pour que le texte associé fournisse un crib contraint.

Ensuite seulement revenir aux primitives, gallows, q/qo et modèles de compression.

**Le but n'est plus de deviner la langue. Le but est de retrouver le document que le Voynich pourrait compresser, adapter ou recopier.**