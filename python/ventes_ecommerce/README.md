# Ventes E-commerce — Étude complète (A à H)

Le projet le plus complet de la série : une étude de bout en bout d'un jeu de données e-commerce, structurée en 8 parties allant de l'exploration à NumPy.

## Contexte

Commandes en ligne avec catégorie de produit, canal de vente, remise, délai de livraison, satisfaction client et statut de commande (livrée, annulée...).

## Fichiers

| Fichier | Description |
|---|---|
| `ventes_ecommerce.csv` | `id_commande`, `date_commande`, `client_id`, `ville_client`, `categorie_produit`, `nom_produit`, `quantite`, `prix_unitaire`, `remise_pourcentage`, `mode_paiement`, `canal_vente`, `delai_livraison_jours`, `note_satisfaction`, `statut_commande` |
| `E_Commerce_Frame.ipynb` | Notebook d'analyse structuré en parties A à H |

## Contenu du notebook

- **A. Exploration** : forme, types, statistiques descriptives, valeurs uniques, répartition par statut
- **B. Nettoyage** : doublons, imputation (médiane par catégorie, ville "Inconnue"), détection et correction des prix aberrants (> 5× la médiane de la catégorie)
- **C. Filtrage et tri** : commandes livrées, top 10 par montant, filtres combinés (catégorie + canal + satisfaction), livraisons lentes mais abouties
- **D. Agrégation** : `montant_total` (avec remise), CA sur commandes livrées uniquement, CA par catégorie, `.agg()` multi-métriques par canal, taux d'annulation par catégorie
- **E. Pivot_table** : CA par catégorie/canal, satisfaction par ville/catégorie, identification de la meilleure combinaison via `.stack().idxmax()`
- **F. Apply/Lambda** : tranches de montant, type de panier, remise fidélité fictive via fonction `def` + `apply`
- **G. Dates et texte** : extraction année/mois/jour de semaine, CA par mois, recherche textuelle avec `.str.contains()`
- **H. NumPy et synthèse** : moyenne, écart-type, 90e percentile avec NumPy ; corrélation délai de livraison / satisfaction

## Résultats clés

- La catégorie "Électronique" est la plus rentable
- Le canal "Site web" est le plus performant (volume, montant moyen, satisfaction)
- Mai est le mois générant le plus de chiffre d'affaires ; le samedi reçoit le plus de commandes
- Un délai de livraison plus long est associé à une moins bonne satisfaction

## Utilisation

```bash
pip install pandas numpy
jupyter notebook E_Commerce_Frame.ipynb
```
