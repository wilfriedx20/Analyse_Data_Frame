# Titanic — Analyse exploratoire

Analyse classique du dataset Titanic (à partir d'un fichier Excel) pour explorer les facteurs liés à la survie des passagers.

## Contexte

Données des passagers du Titanic : classe, sexe, âge et survie. Exercice d'exploration et de nettoyage suivi d'une analyse croisée survie/sexe/classe.

## Fichiers

| Fichier | Description |
|---|---|
| `titanic.xlsx` | Données brutes des passagers |
| `titanic.ipynb` | Notebook d'analyse |

## Contenu du notebook

- Suppression des colonnes peu utiles à l'analyse (`name`, `sibsp`, `parch`, `ticket`, `cabin`, `home.dest`, `body`, `fare`, `boat`, `embarked`)
- Nettoyage : suppression des lignes avec valeurs manquantes (`dropna`)
- Répartition des passagers par classe (`value_counts` + bar plot) et par âge (histogramme)
- Taux de survie moyen, par sexe, puis par sexe **et** classe (`groupby().mean()`)

## Résultats clés

- Le taux de survie global passe de 38% à 40% après nettoyage des valeurs manquantes
- La majorité des passagers avaient entre 18 et 25 ans
- 75% des femmes ont survécu contre 20% des hommes
- Les hommes de 1ère classe ont un taux de survie plus faible que les femmes de 3ème classe (47% vs 35% de mortalité relative)

## Utilisation

```bash
pip install pandas numpy matplotlib openpyxl
jupyter notebook titanic.ipynb
```
