# Cas 2 — Paie : un processus de contrôle de bout en bout

**Données :** `donnees/03-paie/` (12 salariés fictifs, variables de novembre, taux **fictifs**).
**Outil conseillé :** Cowork ou un Projet « Paie ».

> Les taux de cotisation sont inventés pour l’exercice. En vrai, la paie se calcule dans le logiciel de paie avec les taux CAFAT et conventionnels en vigueur. Claude sert ici à **préparer et contrôler**, pas à remplacer le logiciel.

## Le processus

| Étape | Qui | Ce que fait Claude |
| --- | --- | --- |
| 1. Collecte des variables (heures sup, absences, primes) | Managers | Consolide les fichiers reçus, signale les manquants |
| 2. Contrôle de cohérence | Gestionnaire paie | Détecte les anomalies avant saisie |
| 3. Calcul dans le logiciel de paie | Logiciel | — |
| 4. Contrôle post-paie | Gestionnaire paie | Compare au mois précédent, explique les écarts |
| 5. Écritures et déclarations | Comptable | Prépare l’écriture de paie et le récapitulatif |

## Prompts

**Contrôle des variables :**
```text
Croise salaries.xlsx et variables_novembre.xlsx. Liste les anomalies :
heures sup sur un poste de gérant, absences sans motif, prime supérieure à 10 % du salaire de base,
CDD dont la date de fin n’est pas renseignée. Présente un tableau : matricule, anomalie, action proposée.
```

**Simulation pédagogique :**
```text
Avec les taux du fichier taux_cotisations_FICTIFS.xlsx, calcule pour chaque salarié :
brut (base + heures sup à 125 % + prime − absences), cotisations salariales, net, charges patronales.
Puis le total de la masse salariale et l’écriture de paie (641000, 645000, 421000, 431000).
Indique clairement que les taux sont fictifs.
```

## Points de vigilance
- Données nominatives et salaires : **jamais** sur une licence gratuite ou individuelle.
- Dans l’entreprise, l’accès à la paie se cloisonne : un connecteur ne doit pas l’exposer à tous.
