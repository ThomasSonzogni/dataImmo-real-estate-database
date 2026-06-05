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

# Le dictionnaire de données

<img width="1025" height="438" alt="image" src="https://github.com/user-attachments/assets/1b010cb9-ef16-4e4a-9516-9eb921ee833b" />

# Schéma relationnel modifié


<img width="844" height="458" alt="image" src="https://github.com/user-attachments/assets/608ce4bf-d743-4a9d-9ab0-47173fcdb729" />


# Code SQL générant les tables 
 

<img width="945" height="789" alt="image" src="https://github.com/user-attachments/assets/251b169c-a08e-4bb5-82bc-170b0fb11d4f" />


# Capture d’écran base de données chargée

<img width="823" height="320" alt="image" src="https://github.com/user-attachments/assets/6ee93854-8d9a-4326-bca6-9dd24166276d" />

<img width="891" height="38" alt="image" src="https://github.com/user-attachments/assets/e7605f33-3992-45df-8304-9609887163b1" />

<img width="945" height="32" alt="image" src="https://github.com/user-attachments/assets/a05c2ca1-8001-41d4-a5ee-9ded0a93391a" />


# Les requêtes SQL


<img width="871" height="408" alt="image" src="https://github.com/user-attachments/assets/e7789694-e295-4f0e-a1d5-298b0a26ac40" />

<img width="775" height="413" alt="image" src="https://github.com/user-attachments/assets/45545f49-35b7-4f48-9a72-bd81ba2db3d4" />

<img width="787" height="867" alt="image" src="https://github.com/user-attachments/assets/2f8ec71c-3212-4308-afab-a557a372ce1a" />

<img width="765" height="371" alt="image" src="https://github.com/user-attachments/assets/a89a303d-ccaf-4260-ac99-907f8c4e158b" />

<img width="760" height="226" alt="image" src="https://github.com/user-attachments/assets/c90f3d1a-da7c-4718-8a91-69adbf5e87c3" />

<img width="772" height="353" alt="image" src="https://github.com/user-attachments/assets/63088516-6d6c-4a74-a435-35660a49f167" />

<img width="803" height="298" alt="image" src="https://github.com/user-attachments/assets/2ad223c8-a696-492c-a0cb-c5b3d7e21edb" />

<img width="819" height="369" alt="image" src="https://github.com/user-attachments/assets/1a7f3799-7522-4384-9bb7-3bfbcb5ca94f" />

<img width="807" height="277" alt="image" src="https://github.com/user-attachments/assets/a4e8ec1b-dd05-4e2c-bda1-d1fa9883b7c2" />

<img width="836" height="619" alt="image" src="https://github.com/user-attachments/assets/fe0957be-fbd4-40c7-9974-50ce88ec6aff" />

<img width="634" height="731" alt="image" src="https://github.com/user-attachments/assets/c0505c17-c5d6-4426-a4f1-f73d158c503a" />

<img width="568" height="605" alt="image" src="https://github.com/user-attachments/assets/b881aa6d-8628-4aa6-ba3a-9144167e1047" />


