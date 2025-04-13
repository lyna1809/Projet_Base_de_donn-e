# Mission Climat – Gestion et Analyse de Données

Ce projet a pour objectif de gérer et d’analyser des informations relatives aux travaux d'isolation, de chauffage, de photovoltaïque, ainsi qu'aux données administratives (communes, départements) et aux mesures environnementales dans le cadre d'une mission climat.  
L'architecture repose sur la création d'une **base de données SQLite** alimentée par des fichiers CSV et une **application Python** avec interface graphique (Tkinter) pour interagir avec ces données.


## Technologies Utilisées

- **Python 3**  
  Langage principal pour le développement de l'application.

- **SQLite**  
  Système de gestion de base de données léger permettant de stocker et d'interroger les informations.

- **Tkinter**  
  Bibliothèque Python pour la création d'interfaces graphiques.

- **SQL**  
  Langage utilisé pour définir la structure des tables et interroger les données.

---

## Structure du Projet

## Fonctionnalités Réalisées

- ### Base de Données
  - **Création et Structuration**  
    Le module `utils/db.py` gère la création de la base de données SQLite et l'initialisation des tables.  
    **Tables créées :**
    - **Informations Générales :** Tables pour stocker les données .
    - **Données Administratives :** Tables pour gérer les communes et départements.
    - **Mesures Environnementales :** Tables dédiées aux enregistrements de mesures (température, relevés, etc.).
  
  - **Insertion et Suppression**  
    Des scripts permettent l'insertion des données issues des fichiers CSV (situés dans `data/csv/`) et la réinitialisation de la base au besoin.

- ### Interface Graphique et Application Python
  - **Interface Utilisateur avec Tkinter**  
    L'application (dans `main.py`) propose une interface graphique simple et intuitive qui permet de :
    - Créer, insérer et supprimer la base de données.
    - Consulter et afficher les données sous différents angles (requêtes de type F1 à F4 et Q1 à Q7).
  
  - **Requêtes et Analyses**  
    - **Fonctions Fournies (F1 à F4) :** Par exemple, l'affichage des températures moyennes, le filtrage des départements ou l'analyse des mesures sur une période précise.
    - **Questions et Requêtes Avancées (Q1 à Q7) :** Opérations permettant d’extraire des statistiques, d’identifier le département le plus chaud ou de gérer la répartition des travaux.
  
  - **Modularité**  
    La séparation en modules (`actions/` et `utils/`) assure une maintenance aisée et la possibilité d’étendre les fonctionnalités (ajout de nouvelles requêtes, par exemple).

---
