# Cas 1 — Factures d’achat et de vente

**Données :** `donnees/01-factures-achat/` (8 factures PDF, plan comptable, corrigé) et `donnees/02-factures-vente/` (clients, commandes).
**Outil conseillé :** Cowork.

## Partie A — Achats : de la facture papier à l’écriture

1. **Numérisation.** Ouvrez le dossier `pdf/` dans Cowork (en vrai : un scan ou une photo par facture).
2. **Extraction.** Prompt :
   ```text
   Lis chaque facture PDF du dossier. Crée un tableau Excel avec une ligne par facture :
   n° facture, fournisseur, date, échéance, total HT, TGC par taux, total TTC.
   Signale toute facture illisible ou incohérente (HT + TGC ≠ TTC).
   ```
3. **Saisie comptable.** Prompt :
   ```text
   À partir de ce tableau et du plan comptable plan_comptable_extrait.xlsx, propose les écritures
   au journal d’achats : compte de charge ou d’immobilisation, 445660 TGC déductible, 401000 fournisseur.
   Format : date ; journal ; compte ; libellé ; débit ; crédit. Vérifie que chaque écriture est équilibrée.
   ```
4. **Contrôle.** Comparez avec `corrige_saisie_attendue.xlsx`. Où Claude a-t-il hésité (immobilisation ou charge) ?

## Partie B — Ventes : de la commande à la facture

1. Prompt :
   ```text
   À partir de commandes_a_facturer.xlsx et clients.xlsx, crée une facture PDF par client
   regroupant ses commandes du mois, TGC 11 %, mentions de la société fictive Lagon Bleu Équipements.
   Puis prépare les écritures du journal des ventes (411000 / 706000 ou 707000 / 445710).
   ```
2. **Connecteurs.** En entreprise, un connecteur (logiciel de facturation, Drive, messagerie) permet à Claude
   de lire les commandes et de déposer les factures directement. Montrez la page Plug-ins › Connecteurs.

## Points de vigilance
- Claude propose, le comptable valide : aucune écriture n’est passée sans contrôle.
- Une immobilisation (robot, pompe) au-delà du seuil interne ne va pas en charge.
