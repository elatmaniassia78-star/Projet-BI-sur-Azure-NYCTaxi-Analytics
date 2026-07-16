Projet : Pipeline Data Engineering sur Azure - NYC Taxi Analytics
Ce projet a pour objectif de concevoir et d'implémenter un pipeline de données complet (End-to-End) sur Microsoft Azure. Il permet de transformer des données brutes de courses de taxis de New York en insights métier exploitables pour la prise de décision.

🏗️ Architecture du projet
Le projet suit une architecture moderne Raw → Curated :

Ingestion : Collecte des données publiques NYC Taxi vers Azure Data Lake Storage Gen2 (Zone Raw).

Transformation : Nettoyage et enrichissement des données avec Azure Data Factory (Data Flows) (Zone Curated).

Modélisation : Structuration des données selon un schéma en étoile (Star Schema).

Stockage Analytique : Chargement des tables (Fact & Dimensions) dans Azure SQL Database.

Visualisation : Dashboard interactif sur Power BI pour l'analyse des KPI métier.

🛠️ Stack Technique
Cloud : Microsoft Azure

Orchestration & ETL : Azure Data Factory (Copy Activity, Data Flows)

Stockage : Azure Data Lake Storage Gen2 (ADLS Gen2)

Base de données : Azure SQL Database

BI & Analytics : Power BI (DAX, Modélisation)

Format de fichier : Parquet

🚀 Étapes principales du pipeline
Ingestion : Automatisation de la récupération des fichiers via un pipeline ADF.

Transformation (Curated) :

Gestion des valeurs nulles.

Suppression des doublons.

Calcul du revenu total (fare_amount + tip_amount).

Modélisation : Création des tables de faits (fact_trips) et des dimensions (dim_date, dim_zone, dim_payment).

📊 Analyse métier (Dashboard)
Le dashboard Power BI permet de répondre aux questions suivantes :

Quels sont les revenus générés par jour/heure ?

Quelles sont les zones les plus fréquentées ?

Quel est le comportement des clients en termes de pourboires ?

Analyse des heures de pointe.

📂 Structure du dépôt
Plaintext
├── data/               # Exemples de datasets
├── pipeline/           # Scripts et fichiers ARM (ADF)
├── sql/                # Scripts de création des tables SQL
└── README.md           # Documentation du projet
Astuce : Une fois que tu as ajouté ce contenu dans ton fichier README.md sur GitHub, ton dépôt ne sera plus vide et tu pourras finaliser le lien avec Azure Data Factory sans erreur !
