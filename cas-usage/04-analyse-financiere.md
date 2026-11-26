# Cas 4 — Analyse financière poussée et sur mesure

**Données :** `donnees/05-analyse/comptes_3_ans.xlsx` et `budget_vs_reel_2025.xlsx`.
**Outil conseillé :** Chat (modèle Opus) puis artefact Données.

## Prompts

1. **Diagnostic**
   ```text
   Tu es analyste financier. À partir de comptes_3_ans.xlsx, calcule sur 3 ans :
   croissance du CA, taux de marge brute, EBE et taux d’EBE, poids de la masse salariale,
   BFR et BFR en jours de CA, DSO, DPO, rotation des stocks, endettement net / EBE, trésorerie.
   Présente un tableau, puis les 3 constats majeurs et les 3 risques, chiffrés.
   ```
2. **Sur mesure**
   ```text
   Le dirigeant se demande s’il peut embaucher deux techniciens en 2026.
   Quels indicateurs le permettent ou l’en empêchent ? Quelle condition sur le DSO
   libérerait la trésorerie nécessaire ?
   ```
3. **Budget vs réel**
   ```text
   Analyse budget_vs_reel_2025.xlsx : écarts mensuels en valeur et en %, les 3 mois
   les plus atypiques, et un commentaire de gestion de 5 lignes pour le comité de direction.
   ```
4. **Tableau de bord** : « Fais-en un artefact tableau de bord interactif. »

## Points de vigilance
- Demandez toujours le détail des calculs pour pouvoir les vérifier.
