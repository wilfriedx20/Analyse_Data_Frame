# 🦸 MCU Data Analysis - Exploration du Marvel Cinematic Universe

Un petit projet perso pour combiner deux de mes passions : la **data analysis** et l'univers **Marvel**. En tant que fan du MCU, j'avais envie d'aller au-delà du visionnage des films et de creuser un peu dans les chiffres : quels films cartonnent vraiment, quelle phase a été la plus rentable, qui est l'acteur le plus présent dans la franchise... bref, tout ce qu'un fan curieux (et un peu data nerd) a envie de savoir.

## 📊 À propos du projet

Ce notebook explore un dataset regroupant les films du Marvel Cinematic Universe (notes IMDB, box-office, budget, durée, phase, acteur principal, etc.) à l'aide de **Python**, **Pandas** et **Matplotlib**.

## 🔍 Ce qui est analysé

- **Nettoyage des données** : suppression des colonnes non pertinentes pour l'analyse (Metacritic, Rotten Tomatoes, storyline, etc.)
- **Top 10 des films les mieux et moins bien notés sur IMDB**
- **Évolution des profits par année** (avec visualisation en barres)
- **Nombre de projets sortis par année**
- **Évolution des profits par phase du MCU**
- **Détail des productions de la phase la plus rentable**
- **Évolution de la durée moyenne des films au fil des années**
- **L'acteur le plus présent dans la franchise** (lead actor)
- **Liste des films ayant été à perte** (budget > profit)

## 🎬 Quelques découvertes marquantes

- *Avengers: Infinity War* et *Avengers: Endgame* se partagent la première place au classement IMDB
- *The Marvels* ferme la marche... sans grande surprise 😅
- La **Phase 3** est de loin la phase la plus rentable du MCU, portée par un nombre record de productions
- **Robert Downey Jr.** reste l'acteur le plus présent en tant que lead dans la franchise
- Seules **4 productions** ont été déficitaires depuis le début de la Phase 1

## 🛠️ Outils utilisés

- Python
- Pandas
- Matplotlib
- Jupyter Notebook

## 📁 Structure

```
├── mcu.ipynb                    # Notebook d'analyse
├── marvel_movies_dataset.csv    # Dataset utilisé
└── README.md
```

## 🚀 Pour lancer le projet

```bash
pip install pandas matplotlib jupyter
jupyter notebook mcu.ipynb
```

---

*Projet réalisé par passion, entre deux visionnages du MCU dans l'ordre chronologique (oui, ça compte comme de la recherche).* 🍿
