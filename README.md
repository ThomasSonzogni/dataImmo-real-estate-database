# Analyse du marché des assurances habitation
 
## Description
 
Ce projet a pour objectif d'aider une entreprise d'assurance à mieux accompagner ses clients
en analysant le marché des **assurances habitation**.
 
Il couvre l'ensemble de la chaîne de travail d'un data analyst : exploration des données,
modélisation relationnelle, création d'une base de données et rédaction de requêtes SQL.
 
---
 
## Objectifs
 
- Explorer et comprendre les données de contrats clients et le référentiel géographique.
- Construire un **dictionnaire de données** complet (types, contraintes, descriptions).
- Concevoir un **schéma relationnel normalisé** (3NF) et générer le code SQL associé.
- Créer et charger la base de données dans un SGBD (SQLite).
- Rédiger des **requêtes SQL** pour répondre à des analyses métier.
---
 
## Sources de données
 
| Fichier | Contenu |
|---------|---------|
| Données de contrats clients | Informations sur les contrats d'assurance habitation |
| Référentiel géographique | Régions françaises — extrait de [data.gouv.fr](https://www.data.gouv.fr) |
 
---
 
## Outils utilisés
 
| Outil              | Usage                                      |
|--------------------|--------------------------------------------|
| SQLite             | Gestion de la base de données relationnelle |
| SQL Power Architect | Conception du schéma relationnel           |
| Excel              | Exploration et dictionnaire de données     |

 ---
 
## Structure du projet
 
```
Analyse_marche_assurances_habitation/
├── data/
│   ├── Contrat.csv
│   └── Region.csv
│
├── documentation_bdd/
│   ├── dictionnaire_données_thomas_sonzogni.xlsx
│   ├── Document technique projet 3.docx
│   └── projet3oc.sqlite
│
├── presentation/
│   └── presentation.pptx
│
└── README.md
```
 
---
 
## Dictionnaire de données
 
<img width="1025" height="438" alt="Dictionnaire de données" src="https://github.com/user-attachments/assets/1b010cb9-ef16-4e4a-9516-9eb921ee833b" />
---
 
## Schéma relationnel
 
<img width="844" height="458" alt="Schéma relationnel normalisé" src="https://github.com/user-attachments/assets/608ce4bf-d743-4a9d-9ab0-47173fcdb729" />
---
 
## Création des tables — SQLite
 
<img width="945" height="789" alt="Code SQL de création des tables" src="https://github.com/user-attachments/assets/251b169c-a08e-4bb5-82bc-170b0fb11d4f" />
---
 
## Base de données chargée
 
<img width="823" height="320" alt="Base de données chargée" src="https://github.com/user-attachments/assets/6ee93854-8d9a-4326-bca6-9dd24166276d" />
<img width="891" height="38" alt="Nombre de lignes table 1" src="https://github.com/user-attachments/assets/e7605f33-3992-45df-8304-9609887163b1" />
<img width="945" height="32" alt="Nombre de lignes table 2" src="https://github.com/user-attachments/assets/a05c2ca1-8001-41d4-a5ee-9ded0a93391a" />
---
 
## Requêtes SQL
 
### Requête 1
<img width="871" height="408" alt="Requête 1" src="https://github.com/user-attachments/assets/e7789694-e295-4f0e-a1d5-298b0a26ac40" />
### Requête 2
<img width="775" height="413" alt="Requête 2" src="https://github.com/user-attachments/assets/45545f49-35b7-4f48-9a72-bd81ba2db3d4" />
### Requête 3
<img width="787" height="867" alt="Requête 3" src="https://github.com/user-attachments/assets/2f8ec71c-3212-4308-afab-a557a372ce1a" />
### Requête 4 — Top 5 des contrats avec les surfaces les plus élevées
<img width="765" height="371" alt="Requête 4" src="https://github.com/user-attachments/assets/a89a303d-ccaf-4260-ac99-907f8c4e158b" />
### Requête 5 — Prix moyen de la cotisation mensuelle
<img width="760" height="226" alt="Requête 5" src="https://github.com/user-attachments/assets/c90f3d1a-da7c-4718-8a91-69adbf5e87c3" />
### Requête 6 — Nombre de contrats par catégorie de valeur déclarée des biens
<img width="772" height="353" alt="Requête 6" src="https://github.com/user-attachments/assets/63088516-6d6c-4a74-a435-35660a49f167" />
### Requête 7 — Nombre de formules "intégral" en Pays de la Loire
<img width="803" height="298" alt="Requête 7" src="https://github.com/user-attachments/assets/2ad223c8-a696-492c-a0cb-c5b3d7e21edb" />
### Requête 8 — Contrats avec type et formule pour les maisons du département 71
<img width="819" height="369" alt="Requête 8" src="https://github.com/user-attachments/assets/1a7f3799-7522-4384-9bb7-3bfbcb5ca94f" />
### Requête 9 — Surface moyenne des contrats à Paris
<img width="807" height="277" alt="Requête 9" src="https://github.com/user-attachments/assets/a4e8ec1b-dd05-4e2c-bda1-d1fa9883b7c2" />
### Requête 10 — Top 10 des départements avec la cotisation moyenne la plus élevée
<img width="836" height="619" alt="Requête 10" src="https://github.com/user-attachments/assets/fe0957be-fbd4-40c7-9974-50ce88ec6aff" />
### Requête 11 — Communes avec au moins 150 contrats
<img width="634" height="731" alt="Requête 11" src="https://github.com/user-attachments/assets/c0505c17-c5d6-4426-a4f1-f73d158c503a" />
### Requête 12 — Nombre de contrats par région
<img width="568" height="605" alt="Requête 12" src="https://github.com/user-attachments/assets/b881aa6d-8628-4aa6-ba3a-9144167e1047" />
---
 
## Auteur
 
**Thomas Sonzogni**

