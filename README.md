# 🍽️ TP3 – Étude de cas Yelp  
## 420-514-MV — Automne 2025  
### Équipe : Aya Issa, Juba Redjradj, Chadi El-Chami

---

## 📌 1. Présentation du projet
Ce projet analyse une partie du dataset Yelp afin de construire un dataset intégré, calculer plusieurs indicateurs liés aux restaurants, puis créer deux visualisations (dont une interactive) accompagnées d’interprétations.  
L’objectif final est de mieux comprendre la qualité, la popularité, les prix et la satisfaction des restaurants dans différentes villes.

---

## 👥 2. Répartition des tâches (Qui a fait quoi)

### **Aya — Partie 1 : Préparation et chargement des données**
- Initialisation du projet.
- Création de l’arborescence.
- Importation des CSV depuis `Data_use_case_Yelp/`.
- Nettoyage de base, gestion des valeurs manquantes.
- Extraction des attributs demandés dans les tables (business, review, user, ...).

### **Chadi — Partie 2 : Visualisations**
- Création du graphique statique (barres/histogramme).  
- Création du graphique interactif avec `ipywidgets`.  
- Interprétations complètes des deux graphiques.  
- Ajustements visuels, labels, styling.

### **Juba — Partie 3 : Jointures, indicateurs et analyse finale**
- Analyse des jointures entre tables.
- Calcul des indicateurs finaux :  
  `avg_stars`, `review_count_total`, `positive_ratio`, `checkins_total`, `is_chain`, `price`, `elite_users_count`, `avg_open_hours`.  
- Rédaction de l’analyse finale (3–5 observations).

---

## 🧰 3. Librairies Python utilisées

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import ipywidgets as widgets
from ipywidgets import interact
```

---

## 🛠️ 4. Installation (si nécessaire)

### Installation dans Jupyter :
```python
!pip install pandas numpy matplotlib ipywidgets
!jupyter nbextension enable --py widgetsnbextension
```

---

## 🧱 5. Structure du Notebook (tp_yelp.ipynb)

### **1. Introduction**
Présentation du TP, objectifs et description des tables.

### **2. Chargement des données (Aya)**
Importation de toutes les tables depuis le dossier `Data_use_case_Yelp/`.

### **3. Préparation et nettoyage (Aya)**
Nettoyage, conversion de types, extraction des colonnes nécessaires.

### **4. Intégration + Calcul des indicateurs (Juba)**
Jointures entre tables + calcul de :
- moyenne étoiles → `avg_stars`
- total reviews → `review_count_total`
- ratio positifs → `positive_ratio`
- check-ins totaux → `checkins_total`
- chaîne ou non → `is_chain`
- prix → `price`
- nombre d’utilisateurs élite → `elite_users_count`
- heures ouverture moyennes → `avg_open_hours`

### **5. Visualisations (Chadi)**

#### 📊 **Graphique statique — Répartition des prix**
Histogramme montrant combien de restaurants appartiennent à chaque niveau de prix (0–4).  
Interprétation incluse dans le notebook.

#### 🗺️ **Graphique interactif — Meilleurs restaurants par ville**
Menu déroulant pour sélectionner une ville et afficher les meilleurs restaurants (classement par note).

### **6. Analyse & Conclusions (Juba)**
3–5 observations finales basées sur les graphiques + dataset.

---

## 📝 6. Instructions pour exécuter le notebook

1. Extraire le fichier ZIP.  
2. Placer le dossier `Data_use_case_Yelp/` au meme niveau que le notebook (racine).  
3. Ouvrir `tp_yelp.ipynb` dans VSCode ou Jupyter.
4. Copier la commande d'installation des librairies la cellule des imports.
5. Exécuter toutes les cellules (`Run All`).  
