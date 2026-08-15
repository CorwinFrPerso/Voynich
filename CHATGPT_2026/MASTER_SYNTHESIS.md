# MASTER SYNTHESIS

## Mission

Percer le système du manuscrit de Voynich en évitant deux pièges historiques :

1. sur-interpréter des ressemblances linguistiques locales ;
2. explorer un espace d'hypothèses pratiquement infini sans contrainte externe.

## Convictions de travail

- le système paraît uniforme ;
- EVA et v101 sont utiles mais imposent leurs propres segmentations ;
- plusieurs formes semblent construites à partir de primitives récurrentes ;
- les micro-variations scribales doivent être ignorées par défaut ;
- certains gallows et benches peuvent être des constructions, pas des caractères atomiques ;
- q/qo possède une contrainte positionnelle trop forte pour être traité naïvement comme une lettre libre ;
- un mélange vernaculaire germanique + latin technique reste historiquement plausible mais ne doit pas guider la lecture avant le crib.

## Changement stratégique majeur

La stratégie principale est maintenant **CRIB FIRST**.

Le but n'est plus de commencer par `q = ?`, `ch = ?`, ou « quelle langue ? ».

Le but est de retrouver une source documentaire apparentée grâce à l'iconographie, l'ordre des pages, les structures de recettes et les traditions manuscrites.

## Pipeline global

```text
Voynich images + ordre + structure
        ↓
corpus de manuscrits XIVe-XVe
        ↓
recherche de séquences iconographiques / documentaires
        ↓
source candidate
        ↓
texte médiéval associé
        ↓
crib contraint
        ↓
primitives graphiques Voynich
        ↓
modèles de compression / abréviation
        ↓
validation prospective
```

## Couche graphique minimale

Travailler d'abord avec des features robustes :

- c / i / o / 8 / gallows ;
- nombre de hampes ;
- boucle gauche/droite ;
- rail / bench ;
- insertion d'un gallow dans un bench ;
- position initiale/médiane/finale ;
- structure longue traversant un espace.

Ne remonter aux micro-détails qu'après signal statistique fort.

## Familles particulièrement informatives

### c / ch / sh

Ne pas lire `ch` et `sh` comme séquences linguistiques EVA.

Hypothèse visuelle :

- `e ≈ c` ;
- `ch ≈ cc + rail` ;
- `sh ≈ cc + rail + marque supérieure`.

### gallows

Relations de travail :

- `p = f + boucle gauche` ;
- `t = k + boucle gauche`.

Tester si la même transformation graphique a le même effet fonctionnel sur plusieurs bases.

### q / qo

Tester prioritairement :

- préfixe ;
- classe ;
- macro ;
- opcode ;
- mode de reconstruction.

### split gallows

Tester si les grands gallows sont des opérateurs de portée/factorisation plutôt que des caractères géants.

## Modèles de codage concurrents

1. sténographie morphographique / mnémotechnique ;
2. syllabaire featural ;
3. base consonantique + information vocalique distribuée ;
4. hybride phonétique + opérateurs sémantiques ;
5. substitution classique, modèle de contrôle.

## Critère de vérité

Aucune lecture locale ne suffit.

Une hypothèse doit :

1. expliquer plusieurs familles avec peu de règles ;
2. conserver les contraintes positionnelles ;
3. produire une meilleure compression/prédiction ;
4. fonctionner hors échantillon ;
5. prédire des pages ou structures non utilisées lors de sa découverte.

## Premier objectif concret

Trouver dans Herbal A, la balnéologie ou l'astro-médecine une **séquence documentaire multi-page** dont l'ordre est trop proche d'une source médiévale pour être dû au hasard.

Une fois cette source trouvée, le texte associé devient notre premier crib sérieux.

## Règle d'humilité

600 ans d'échecs ne signifient pas que le système est surnaturel. Ils signifient surtout qu'une stratégie capable de générer trop facilement des histoires plausibles est dangereuse.

Notre méthode doit donc maximiser les contraintes externes avant de maximiser l'ingéniosité du décodage.