# Cas 5 — Prévisionnel interactif avec curseurs

**Données :** `donnees/06-previsionnel/hypotheses.xlsx` (valeurs de départ et bornes des curseurs).
**Outil conseillé :** Chat › artefact.

## Prompt

```text
Crée un artefact interactif « Prévisionnel 2026-2028 » pour Lagon Bleu Équipements (fictif).
Utilise les hypothèses du fichier hypotheses.xlsx :
- un curseur par hypothèse, avec les bornes min et max du fichier ;
- un compte de résultat prévisionnel sur 3 ans (CA, marge brute, charges de personnel, EBE, résultat) ;
- un plan de trésorerie mensuel 2026 qui tient compte des délais clients et fournisseurs ;
- un graphique de trésorerie qui se met à jour quand on bouge un curseur ;
- une alerte visible si la trésorerie passe sous zéro.
Montants en XPF. Ajoute un bouton « Scénario prudent » et « Scénario ambitieux ».
```

## À faire pendant l’exercice
1. Bougez le curseur « Délai client » de 45 à 75 jours : que devient la trésorerie ?
2. Ajoutez 4 embauches : à partir de quel mois faut-il un financement ?
3. Demandez à Claude d’ajouter une hypothèse de votre choix.

## Points de vigilance
- Un prévisionnel vaut ce que valent ses hypothèses : notez-les dans votre second cerveau.
