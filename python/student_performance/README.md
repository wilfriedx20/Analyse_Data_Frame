# Student Performance — Facteurs de réussite scolaire

Analyse d'un dataset d'étudiants pour identifier les facteurs liés à la réussite aux examens : temps d'étude, sommeil, job à temps partiel, accès à internet, niveau d'éducation des parents.

## Contexte

Dataset contenant, pour chaque étudiant, ses habitudes (heures d'étude, présence, sommeil), son contexte socio-familial (job, internet, éducation des parents) et ses résultats (note précédente, note finale, grade).

## Fichiers

| Fichier | Description |
|---|---|
| `student_performance_dataset.csv` | Données brutes (colonnes en anglais) |
| `student_performance.ipynb` | Notebook d'analyse |

## Contenu du notebook

- **Exploration & nettoyage** : renommage de colonnes (`presence_pct`, `activites_extra`, `heures_etude`), `info()`, `describe()`, vérification des valeurs manquantes/dupliquées et des valeurs aberrantes
- **Statistiques** : moyenne/médiane des notes finales, répartition par genre et par grade
- **Analyse croisée** : impact du job à temps partiel, de l'accès à internet et du niveau d'éducation des parents sur la note finale
- **Colonnes dérivées** : `progression` (évolution note précédente → finale), catégorisation du sommeil (`Insuffisant`/`Correct`/`Optimale`) via `apply()`

## Résultats clés

- Les élèves avec un job à temps partiel ont une moyenne finale plus basse
- Les élèves ayant accès à internet ont, de façon surprenante, une meilleure moyenne
- Plus le niveau d'éducation des parents est élevé, plus la moyenne tend à augmenter
- Plus d'un quart des élèves dorment un temps jugé insuffisant

## Utilisation

```bash
pip install pandas matplotlib
jupyter notebook student_performance.ipynb
```
