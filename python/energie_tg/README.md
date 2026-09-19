# ⚡ Analyse de la consommation et production d'énergie au Togo

Exercice d'analyse de données avec **pandas**

## 📋 Contexte

Le secteur de l'énergie au Togo repose sur plusieurs sources : thermique, hydraulique (barrage de Nangbéto), solaire (centrale de Blitta), éolien et biomasse. Plusieurs fournisseurs interviennent sur le marché, dont la **CEET** (Compagnie Énergie Électrique du Togo) et la **CEB** (Communauté Électrique du Bénin).

Ce jeu de données simule des relevés de consommation et de production d'énergie collectés dans les cinq régions du pays (Maritime, Plateaux, Centrale, Kara, Savanes). Comme souvent sur le terrain, ces relevés comportent des erreurs de saisie, des doublons, des valeurs manquantes et des incohérences de casse — l'objectif est de nettoyer ce jeu de données puis d'en tirer des indicateurs exploitables.

## 📁 Contenu du dossier

| Fichier | Description |
|---|---|
| `energie_togo.csv` | Dataset brut (223 lignes, 12 colonnes) avec imperfections volontaires |
| `energie_togo_consignes.pdf` | Consignes de l'exercice + correction complète (code) |

## 🗂️ Description des colonnes

| Colonne | Description |
|---|---|
| `id_releve` | Identifiant unique du relevé |
| `region` | Région administrative (Maritime, Plateaux, Centrale, Kara, Savanes) |
| `prefecture` | Préfecture associée à la région |
| `localite` | Localité du relevé |
| `type_energie` | Thermique, Hydraulique, Solaire, Eolienne, Biomasse |
| `fournisseur` | CEET, CEB, AGAHR, ZAGNABORI SOLAR |
| `date_releve` | Date du relevé (formats non harmonisés) |
| `consommation_kwh` | Consommation relevée en kWh |
| `production_kwh` | Production relevée en kWh |
| `nombre_menages_raccordes` | Nombre de ménages raccordés au réseau |
| `taux_couverture_pourcent` | Taux de couverture électrique de la zone (%) |
| `panne_signalee` | Oui / Non |

## ⚠️ Imperfections volontaires

- Valeurs manquantes sur `fournisseur`, `consommation_kwh`, `production_kwh`, `taux_couverture_pourcent`
- Doublons stricts et quasi-doublons
- Casse incohérente sur les colonnes textuelles (`region`, `prefecture`, `localite`, `type_energie`)
- Formats de date mélangés (`YYYY-MM-DD`, `DD/MM/YYYY`, `DD-MM-YYYY`)

## 🎯 Objectifs de l'exercice

1. Explorer le dataset (dimensions, types, valeurs manquantes, doublons)
2. Nettoyer le dataset (casse, doublons, valeurs manquantes)
3. Harmoniser les dates et en extraire année / mois
4. Calculer des indicateurs moyens par région
5. Calculer un bilan énergétique par relevé (production − consommation)
6. Catégoriser chaque relevé (Excédentaire / Déficitaire)
7. Identifier la région au bilan cumulé le plus déficitaire
8. Construire un tableau croisé dynamique région × type d'énergie
9. Lister les 5 relevés les plus déficitaires
10. Calculer le taux de pannes signalées, global et par région

Le détail complet de chaque objectif ainsi que la correction (code uniquement) se trouvent dans `energie_togo_consignes.pdf`.

## 🛠️ Compétences mobilisées

`isna()` · `duplicated()` / `drop_duplicates()` · `str.title()` · `fillna()` · `groupby().agg()` · `pd.to_datetime()` · `.dt` · `apply()` / `lambda` · `pivot_table()` · `sort_values()`

## ▶️ Utilisation

```bash
pip install pandas numpy
```

```python
import pandas as pd
df = pd.read_csv("energie_togo.csv")
```

---

*Exercice réalisé dans le cadre d'un parcours d'apprentissage de la data analyse avec Python.*
