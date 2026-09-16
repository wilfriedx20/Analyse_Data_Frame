# Ventes Boutique - Nettoyage, agrégation et visualisation

Exercice complet sur un jeu de données de ventes en boutique : exploration, nettoyage de valeurs manquantes/aberrantes, agrégations et visualisations avec Matplotlib.

## Contexte

Commandes passées dans une boutique physique, avec produit, catégorie, quantité, prix unitaire, ville du client et note de satisfaction. Le jeu de données contient volontairement des doublons, valeurs manquantes et valeurs aberrantes.

## Fichiers

| Fichier | Description |
|---|---|
| `ventes_boutique.csv` | `id_commande`, `date_commande`, `client_id`, `ville_client`, `produit`, `categorie`, `quantite`, `prix_unitaire`, `note_satisfaction` |
| `ventes_boutiques.ipynb` | Notebook d'analyse |

## Contenu du notebook

- **Exploration** : `shape`, `dtypes`, `info()`, valeurs manquantes/dupliquées
- **Nettoyage** : suppression des doublons, harmonisation de la colonne `produit` (espaces, casse), conversion de `date_commande`, imputation des valeurs manquantes (médiane par produit pour `prix_unitaire`, valeur par défaut pour `quantite` et `ville_client`), traitement des prix aberrants (> 300)
- **Agrégation** : colonne `montant_total`, extraction de `mois`/`jour_semaine`, chiffre d'affaires par catégorie/mois, `pivot_table` (CA par ville et catégorie), top 5 clients
- **Visualisation** : courbe du CA mensuel, bar plot du CA par catégorie et par ville, superposition de deux courbes de CA par catégorie

## Résultats clés

- La catégorie "Haut" génère le CA le plus élevé, "Bas" le plus faible
- Octobre est le mois avec le plus fort chiffre d'affaires
- La satisfaction moyenne se situe entre 3,46 et 3,89 selon les produits

## Utilisation

```bash
pip install pandas matplotlib
jupyter notebook ventes_boutiques.ipynb
```
