# Synthèse - Agriculture au Togo (Producteurs, Récoltes, Ventes)

Exercice de synthèse combinant l'ensemble des notions vues jusqu'ici (exploration, nettoyage, `groupby`/`agg`, `pivot_table`, `apply`/`lambda`, dates, chaînes, NumPy) avec l'utilisation de **`pd.merge()`** sur **3 tables liées**.

## Contexte

Données fictives (mais réalistes) sur des producteurs agricoles togolais, leurs récoltes et les ventes réalisées sur différents marchés.

## Fichiers

| Fichier | Description | Clé(s) |
|---|---|---|
| `producteurs.csv` | Identité et exploitation de chaque producteur | `producteur_id` |
| `recoltes.csv` | Récoltes réalisées (culture, date, quantité) | `recolte_id`, `producteur_id` |
| `ventes.csv` | Ventes réalisées sur les marchés | `vente_id`, `recolte_id` |

**Relation entre les tables :** `producteurs → recoltes → ventes` (un producteur a plusieurs récoltes, une récolte peut donner lieu à plusieurs ventes).

## Compétences mobilisées

- Exploration : `shape`, `info()`, `isna().sum()`, `isin()`
- Nettoyage : `drop_duplicates()`, `fillna()`, uniformisation de texte (`.str`)
- **Jointures** : `pd.merge()` en cascade (deux jointures successives, `how='inner'`)
- Colonnes dérivées : calculs, `.dt` (dates), `apply()` + fonction `def` avec `axis=1`
- Agrégation : `groupby().agg()`, `pivot_table()`
- NumPy : `np.mean`, `np.median`, `np.std`, détection de valeurs atypiques

## Imperfections volontaires dans les données

- Doublons dans les 3 tables
- Casse incohérente sur la colonne `region`
- Valeurs manquantes sur `superficie_ha` et `quantite_kg`
- Identifiants invalides (`producteur_id` et `recolte_id` qui n'existent pas dans la table référencée)

## Utilisation

```bash
pip install pandas numpy
```
