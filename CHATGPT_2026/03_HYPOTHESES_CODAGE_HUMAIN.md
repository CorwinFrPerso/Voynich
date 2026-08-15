# Hypothèses de codage humain

## Idée générale

Le système Voynich est uniforme du début à la fin. Avant d'imaginer un mécanisme cryptographique sophistiqué, tester des règles qu'un humain du XVe siècle pouvait apprendre, écrire et relire facilement.

Le modèle doit utiliser un petit nombre de primitives robustes et tolérer naturellement les variations de plume.

## H1 : sténographie morphographique / mnémotechnique

Modèle principal actuel.

Structure abstraite :

```text
[classe/préfixe] + [radical comprimé] + [terminaison]
```

Règles possibles :

1. suppression de voyelles prévisibles ;
2. radicaux très fréquents réduits à des blocs graphiques ;
3. terminaisons fréquentes représentées par quelques signes finaux ;
4. rails/benches utilisés comme cadres locaux ;
5. gallows sélectionnant une variante d'un bloc ;
6. boucles modifiant systématiquement la fonction d'une base ;
7. certains signes initiaux servant de classe, préfixe ou mode de lecture.

Cette famille explique naturellement :

- contraintes fortes de position ;
- nombreux mots proches les uns des autres ;
- répétitions locales ;
- familles graphiques régulières ;
- texte compact mais relisible par un initié.

## H2 : syllabaire featural

Les glyphes ne seraient pas des lettres mais des blocs porteurs de plusieurs dimensions.

Exemple abstrait :

- forme de base = squelette consonantique ;
- boucle = voyelle ou classe vocalique ;
- seconde hampe = modification consonantique ;
- rail = fusion ou encadrement d'un bloc ;
- finale = terminaison grammaticale.

Cela permet un « mélange vocalique » sans glyphe vocalique indépendant.

## H3 : système hybride phonétique + opérateurs sémantiques

Dans un manuel pratique, une grande partie du langage est répétitive :

- prendre ;
- appliquer ;
- boire ;
- mélanger ;
- contre/pour une affection ;
- quantité ;
- moment ;
- partie du corps ;
- ingrédient.

Certains signes peuvent donc encoder une opération entière plutôt qu'un son.

Les formes longues pourraient être des opérateurs de portée sur plusieurs chunks.

## H4 : mélange vernaculaire germanique + latin technique

Hypothèse linguistique candidate, pas conclusion.

Scénario :

- vernaculaire germanique pour la langue pratique ;
- latin pour le vocabulaire savant, médical, botanique, astrologique ;
- même système graphique d'abréviation appliqué aux deux.

Familles candidates à comparer ultérieurement :

- Frühneuhochdeutsch / Early New High German ;
- variétés alémaniques ;
- bavaroises ;
- franconiennes ;
- latin médical médiéval ;
- corpus mixtes allemand-latin.

Ne pas choisir un dialecte avant d'avoir identifié une fonction graphique stable ou un crib.

## Propriété structurante : q / qo

Observation à traiter comme prioritaire :

- EVA-q apparaît presque toujours en début de groupe ;
- `qo` est très fréquent.

Donc `q` doit être testé d'abord comme :

- préfixe ;
- marqueur de classe ;
- opcode ;
- mode de reconstruction ;
- composant d'un macro `qo`.

Éviter `q = lettre X` tant que les contraintes positionnelles restent inexpliquées.

## Expériences mentales avec des formules médiévales

Ces exemples ne sont **pas des traductions**. Ils servent à vérifier qu'un mécanisme humain simple peut produire une morphologie de type Voynich.

### `Contra febrem`

Une formule fréquente peut être condensée en :

```text
[marqueur de fonction] [radical contracté] [terminaison]
```

### `Ad dolorem capitis`

Structure très prévisible :

```text
[indication] + [affection] + [partie du corps]
```

Un lecteur connaissant le domaine peut reconstruire beaucoup avec peu de signes.

### `Recipe X et Y, ana ...`

Une seule indication peut porter sur plusieurs ingrédients. Ce type de logique rend humainement plausible un opérateur graphique ayant portée sur deux chunks.

## Hiérarchie actuelle

1. H1 sténographie morphographique : **prioritaire**.
2. H2 syllabaire featural : **très sérieux**.
3. H3 hybride phonétique + opérateurs : **très sérieux**, surtout pour les formes longues.
4. H4 substitution classique lettre à lettre : **faible** en l'état.
5. chaque micro-variante graphique significative : **rejetée par défaut**.

## Règle anti-surinterprétation

Un mot reconnaissable en latin ou allemand ne vaut rien seul.

Une hypothèse n'est intéressante que si elle :

1. compresse plusieurs familles de formes avec peu de règles ;
2. prédit les contextes ;
3. fonctionne sur du texte non utilisé pour la construire ;
4. bat des langues et modèles témoins.