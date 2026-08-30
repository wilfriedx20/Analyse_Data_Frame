# Iris — Découverte de Seaborn

Petit exercice de prise en main de **Seaborn** à partir du célèbre dataset Iris, pour s'entraîner à visualiser des relations entre variables numériques et une variable catégorielle.

## Contexte

Le dataset Iris contient les mesures de sépales et pétales de 3 variétés de fleurs (setosa, versicolor, virginica). Il sert ici de terrain d'entraînement pour la logique commune aux fonctions Seaborn : `sns.fonction(x, y, data, hue, size, style)`.

## Fichiers

| Fichier | Description |
|---|---|
| `iris.csv` | Dimensions des sépales/pétales (`sepal_length`, `sepal_width`, `petal_length`, `petal_width`) et variété (`species`) |
| `iris_sns.ipynb` | Notebook de visualisation |

## Contenu du notebook

- `sns.pairplot(iris)` : relations entre toutes les variables
- `sns.pairplot(iris, hue='species')` : répartition suivant les variétés

## Observation clé

Les dimensions des pétales suffisent à distinguer la variété *setosa* des deux autres : aucune zone de recouvrement entre les histogrammes sur ces variables.

## Utilisation

```bash
pip install pandas seaborn
jupyter notebook iris_sns.ipynb
```
