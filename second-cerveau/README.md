# Se créer un second cerveau avec Claude

**Objectif :** donner à Claude une mémoire de qualité, que **vous** possédez, sous forme de fichiers texte `.md`. Ces fichiers ne dépendent d’aucun outil : vous pouvez les relire, les corriger, les déplacer, et les donner à Claude (Projet, Cowork ou Code).

## Pourquoi des fichiers `.md` ?

- La mémoire automatique de Claude est utile, mais vous ne la maîtrisez pas entièrement.
- Un fichier `.md` est du texte simple : lisible par vous, par Claude, et par n’importe quel autre outil.
- Vous décidez de ce qui entre, de ce qui sort, et de ce qui est confidentiel.

## La structure

```
mon-second-cerveau/
├── CLAUDE.md            ← les règles que Claude lit en premier
├── 00-index.md          ← la carte de tous les fichiers
├── moi.md               ← mon poste, mes responsabilités, ma façon de travailler
├── entreprise.md        ← l’entreprise, ses chiffres clés, ses outils
├── processus/
│   ├── cloture-mensuelle.md
│   ├── paie.md
│   └── ...
├── glossaire.md         ← les sigles et le vocabulaire maison
└── decisions.md         ← le journal des décisions et de leurs raisons
```

Des modèles prêts à remplir sont dans [`modeles/`](modeles/).

## Étape 1 — Copier-coller ce prompt dans Claude

Ouvrez **Cowork** (ou un **Projet** dans Claude Chat) et collez :

```text
Tu vas m’aider à construire mon « second cerveau » : un ensemble de fichiers Markdown (.md) qui te serviront de mémoire durable.

1. Pose-moi des questions, une rubrique à la fois, pour remplir ces fichiers :
   CLAUDE.md, 00-index.md, moi.md, entreprise.md, glossaire.md, decisions.md,
   et un fichier par processus dans le dossier processus/.
2. Utilise les modèles fournis dans le dossier modeles/ (même structure, mêmes titres).
3. Écris des phrases courtes et factuelles. Pas de données personnelles de salariés,
   pas de montants de salaires, pas de mots de passe : remplace-les par [À COMPLÉTER].
4. Quand une rubrique est finie, crée le fichier, montre-le-moi et attends ma validation.
5. À la fin, mets à jour 00-index.md avec un lien et une ligne de description par fichier.

Commence par moi.md.
```

## Étape 2 — Documenter un processus

Pour chaque processus que vous faites régulièrement, collez :

```text
Je vais te décrire mon processus de [nom du processus] à voix haute, dans le désordre.
Transforme ma description en fichier processus/[nom].md en suivant le modèle modeles/processus.md :
déclencheur, entrées, étapes numérotées, contrôles, sorties, pièges connus, outils.
Pose-moi les questions qui manquent avant d’écrire.
```

## Étape 3 — Faire vivre la mémoire

À la fin d’une session de travail importante :

```text
Relis notre échange. Propose les mises à jour à faire dans mes fichiers .md
(nouvelles décisions, étapes de processus corrigées, termes du glossaire).
Montre-moi les modifications avant de les écrire.
```

## Règles d’or

1. **Un fichier = un sujet.** Un fichier court se relit, un fichier long s’oublie.
2. **Rien de confidentiel** : pas de salaires nominatifs, pas d’IBAN, pas de mots de passe.
3. **Vous validez** chaque fichier avant qu’il soit enregistré.
4. **Une relecture par mois** : supprimer ce qui est faux ou dépassé.
