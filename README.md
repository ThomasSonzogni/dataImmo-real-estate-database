# DATAImmo — Base de données immobilières

> Projet réalisé dans le cadre du réseau national d'agences immobilières **Laplace Immo**.

---

## Contexte

Laplace Immo lance le projet stratégique **DATAImmo** pour développer une base de données
permettant d'analyser le marché immobilier et d'améliorer la prévision des prix de vente,
afin d'accompagner efficacement les agences régionales.

---

## Objectifs

1. **Création de la base de données** — intégration des données de transactions immobilières,
   démographiques et géographiques.
2. **Normalisation** — conception d'un schéma relationnel conforme à la **3NF** (Troisième Forme Normale).
3. **Analyse des données** — utilisation des données du premier semestre 2020 comme POC
   (*Proof of Concept*) pour valider le modèle.
4. **Conformité RGPD** — anonymisation et sécurisation de toutes les données collectées.

---

## Sources de données

| Source | Contenu |
|--------|---------|
| [DVF (data.gouv.fr)](https://www.data.gouv.fr/fr/datasets/demandes-de-valeurs-foncieres/) | Transactions immobilières et foncières en France |
| INSEE | Résultats des recensements de la population |
| data.gouv.fr | Référentiel géographique français (communes, départements, régions) |

---

## Conformité RGPD

La colonne `Nom de l'acquéreur` a été supprimée de la base afin d'assurer l'anonymisation
des données et garantir la conformité au Règlement Général sur la Protection des Données.

---

## Modélisation

Les données sont réparties dans **cinq tables** :

- `REGION` — référentiel des régions françaises
- `DEPARTEMENT` — référentiel des départements
- `COMMUNES` — données communales et démographiques (INSEE)
- `BIENS` — caractéristiques des biens immobiliers
- `VENTES` — historique des transactions

Le schéma relationnel est disponible dans `documentation_bdd/schema_relationnel_base_de_donnee_immo.png`.

---

## Outils utilisés

| Outil | Usage |
|-------|-------|
| SQLite | Gestion de la base de données relationnelle |
| Excel | Dictionnaire de données et analyse préliminaire |
| Draw.io | Création du schéma relationnel |

---

## Requêtes SQL réalisées

1. Nombre total d'appartements vendus au 1er semestre 2020
2. Nombre de ventes d'appartements par région au 1er semestre 2020
3. Proportion des ventes d'appartements par nombre de pièces
4. Top 10 des départements avec le prix au m² le plus élevé
5. Prix moyen du m² d'une maison en Île-de-France
6. Top 10 des appartements les plus chers (avec région et surface)
7. Taux d'évolution des ventes entre le T1 et le T2 2020
8. Classement des régions par prix au m² pour les appartements de plus de 4 pièces
9. Communes ayant enregistré au moins 50 ventes au 1er trimestre
10. Différence de prix au m² entre un appartement 2 pièces et 3 pièces
11. Moyennes des valeurs foncières pour le top 3 des communes des départements 6, 13, 33, 59 et 69
12. Top 20 des communes avec le plus de transactions pour 1 000 habitants (communes > 10 000 hab.)

**Requêtes optionnelles :**
- Top 5 des communes avec la plus grande variation de prix au m² entre le T1 et le T2 2020
- Superficie moyenne des terrains de maisons par région en 2020

---

## Résultats clés — 1er semestre 2020

- **Région parisienne** : plus grand nombre de ventes immobilières en France.
- **Évolution trimestrielle** : hausse des ventes entre le T1 et le T2 2020.
- **Surface / Prix au m²** : plus la surface augmente, plus le prix au m² tend à diminuer.
- **Centre-Val de Loire** : région avec la plus grande superficie de terrain vendue.

---

## Structure du projet

```
dataImmo-real-estate-database/
├── data/                               # Données sources (CSV)
│   ├── biens.csv
│   ├── communes.csv
│   ├── departement.csv
│   ├── region.csv
│   ├── ventes.csv
│   └── donnees_de_base.zip
│
├── documentation_bdd/                  # Documentation de la base
│   ├── bdd_sql/                        # Fichier de la base SQLite
│   ├── Dictionnaire_de_donnees.xlsx
│   └── schema_relationnel_base_de_donnee_immo.png
│
├── presentation/
│   └── support_presentation_requete_base_immo.pptx
│
├── requetes/                           # Scripts SQL
│   ├── creation_bdd.sql
│   └── requetes_bdd.sql
│
├── .gitignore
└── README.md
```

---

## Auteur

**Thomas Sonzogni**
