# Jointure Santé — Patients & Consultations

Exercice dédié à la maîtrise des **jointures avec `pd.merge()`** (inner, left, right, outer) à travers un cas de données médicales fictives.

## Contexte

Deux tables liées par `patient_id` : des patients et leurs consultations médicales. Certains identifiants sont volontairement incohérents pour illustrer les différences entre les types de jointure.

## Fichiers

| Fichier | Description | Clé |
|---|---|---|
| `patients.csv` | Identité et ville des patients | `patient_id` |
| `consultations.csv` | Consultations (médecin, motif, coût) | `consultation_id`, `patient_id` |
| `jointure_sante.ipynb` | Notebook d'analyse |

## Contenu du notebook

- Exploration et nettoyage : `isna()`, `duplicated()`, `drop_duplicates()`, uniformisation de la colonne `ville`
- **Jointure interne** (`how='inner'`) : ne garde que les `patient_id` valides des deux côtés
- **Jointure gauche** (`how='left'`) : révèle les consultations avec un `patient_id` invalide
- **Jointure droite** (`how='right'`) : révèle les patients sans consultation
- **Jointure complète** (`how='outer'`) : combine les deux cas précédents
- Analyse post-jointure : coût total par ville, nombre de consultations par médecin, motif le plus fréquent par ville

## Résultats clés

- 2 `patient_id` invalides dans `consultations.csv`
- 8 patients n'ont aucune consultation enregistrée

## Utilisation

```bash
pip install pandas
jupyter notebook jointure_sante.ipynb
```
