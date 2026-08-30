# Météo Togo 2024 — Visualisation avec Matplotlib

Exercice de visualisation autour de données météo fictives sur plusieurs villes du Togo, pour pratiquer les graphiques en ligne, en barres et en camembert avec **Matplotlib**.

## Contexte

Températures moyennes et précipitations mensuelles pour l'année 2024, relevées sur plusieurs villes togolaises (Lomé, Kara, Sokodé, Kpalimé, Atakpamé, Dapaong...).

## Fichiers

| Fichier | Description |
|---|---|
| `meteo_togo_2024.csv` | `ville`, `mois`, `mois_num`, `temperature_moy_c`, `precipitations_mm` |
| `meteo.ipynb` | Notebook de visualisation |

## Contenu du notebook

- **Line plot** : température moyenne mensuelle pour Lomé, puis superposition avec Kara
- **Bar plot** : précipitations totales annuelles par ville, avec mise en avant de la ville la plus pluvieuse
- **Pie chart** : répartition des précipitations totales entre villes, avec pourcentages (`autopct`)
- **Analyse** : ville la plus contrastée thermiquement, ville la moins arrosée sur l'année

## Résultats clés

- **Sokodé** est la ville la plus contrastée thermiquement (pic en juin, creux en décembre)
- **Dapaong** reçoit le moins de pluie sur l'année

## Utilisation

```bash
pip install pandas matplotlib
jupyter notebook meteo.ipynb
```
