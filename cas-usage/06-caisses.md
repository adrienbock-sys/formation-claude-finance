# Cas 6 — Extraction et rapprochement des caisses

**Données :** `donnees/07-caisses/` — deux magasins fictifs (Nouméa Ducos, 2 caisses ; Païta, 1 caisse), novembre 2026 :
- `export_tickets_novembre.xlsx` : 1 290 tickets environ (extraction du logiciel de caisse) ;
- `tickets_Z.xlsx` : clôtures journalières par caisse ;
- `releve_bancaire_remises_cb.xlsx` : remises carte bancaire sur le relevé.

Trois écarts ont été cachés volontairement dans les données. À vous de les trouver avec Claude.

**Outil conseillé :** Cowork, puis Code pour automatiser.

## Le processus réel
1. Chaque soir, la caisse édite un **ticket Z** (total par mode de paiement).
2. Le lendemain, la banque crédite la **remise CB** (moins la commission).
3. Le comptable rapproche : tickets ↔ Z ↔ banque, et passe l’écriture de ventes et d’encaissement.

## Prompts

**Rapprochement :**
```text
Rapproche les trois fichiers du dossier 07-caisses :
1. somme des tickets par jour, magasin, caisse et mode de paiement, comparée aux tickets Z ;
2. Z carte bancaire comparé à la remise CB du relevé (date de valeur J+1) ;
Liste chaque écart supérieur à 0 XPF : date, magasin, caisse, nature, montant, explication probable.
```

**Écritures :**
```text
Prépare l’écriture de ventes mensuelle par magasin (530000 caisse, 512000 banque, 627800 commissions,
707000 ventes, 445710 TGC collectée) et le tableau de synthèse pour le DAF.
```

**Automatisation (Code) :**
```text
Écris un script qui fait ce rapprochement chaque matin sur le nouvel export,
en lecture seule sur la base de données, et m’envoie un résumé des écarts.
```

## Points de vigilance (cas réel)
- Un accès direct à la base SQL du logiciel de gestion donne accès à **toutes** les tables :
  créez un compte en **lecture seule**, limité aux tables de caisse, et interdisez les requêtes de modification.
- Les droits se règlent par utilisateur : un vendeur ne doit pas lire la comptabilité.
