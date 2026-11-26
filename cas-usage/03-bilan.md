# Cas 3 — Du bilan comptable à partir d’une balance

**Données :** `donnees/04-bilan/balance_generale_2025.xlsx` (balance fictive au 31/12/2025).
**Outil conseillé :** Chat avec analyse de fichier, puis artefact.

## Prompts

1. **Contrôle de la balance**
   ```text
   Vérifie que la balance est exploitable : total débits = total crédits.
   Calcule le résultat de l’exercice (produits de classe 7 − charges de classe 6).
   ```
2. **Bilan et compte de résultat**
   ```text
   Classe chaque compte selon le plan comptable (classes 1 à 7) et présente :
   un bilan actif / passif simplifié et un compte de résultat en cascade
   (marge commerciale, valeur ajoutée, EBE, résultat d’exploitation, résultat net).
   Montre le tableau de passage compte par compte.
   ```
3. **Livrable**
   ```text
   Fais-en un artefact Document « Comptes annuels 2025 » prêt à relire par l’expert-comptable,
   avec les points à confirmer en fin de document.
   ```

## Points de vigilance
- Le résultat doit équilibrer le bilan : c’est le contrôle n° 1. Indice : l’exercice 2025 est légèrement déficitaire.
- Claude ne remplace ni l’expert-comptable ni les écritures d’inventaire (provisions, cut-off).
