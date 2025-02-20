# Weather & Electricity Consumption Analysis

## Description du projet
Ce projet analyse l'impact des conditions météorologiques sur la consommation d'électricité en utilisant **Apache Spark** pour le traitement des données et **Streamlit** pour la visualisation des résultats. Les données météorologiques sont collectées toutes les 3 heures de 2013 à 2022 et sont croisées avec la consommation d'électricité.

Le projet comporte deux parties :
1. **Analyse de l'impact de la météo sur la consommation d'électricité**
2. **Analyse de données météorologiques massives via API**

## Structure du projet
Le projet est organisé comme suit :

```
weather-analysis-with-spark/
│-- bigdata_env/               # Environnement virtuel (à ignorer)
│-- data/                      # Dossier contenant les fichiers de données
│-- docs/                      # Documentation du projet
│   │-- API_usage.docx         # Documentation sur l'usage des API
│   │-- apicds.txt             # Détails des API utilisées
│   │-- packages.txt           # Liste des packages utilisés
│   │-- requirements.txt       # Dépendances Python
│-- df.py                      # Fonctions utilisées dans l'application
│-- script_analyse.ipynb       # Notebook contenant l'analyse des données
│-- wheather_electricity.py    # Script principal de l'application Streamlit
│-- analyse_avec_API.ipynb     # Notebook (zippé en raison de la taille) pour le traitement des données API
│-- .gitignore                 # Fichier pour ignorer certains fichiers/dossiers dans Git
```

## Installation et exécution en local

### Prérequis
- Python 3.8+
- Apache Spark
- pip
- virtualenv (optionnel)

### Étapes d'installation

1. **Cloner le dépôt**
   ```sh
   git clone https://github.com/votre-repo/weather-analysis-with-spark.git
   cd weather-analysis-with-spark
   ```

2. **Créer un environnement virtuel (optionnel mais recommandé)**
   ```sh
   python -m venv bigdata_env
   source bigdata_env/bin/activate   # Pour Linux/Mac
   bigdata_env\Scripts\activate      # Pour Windows
   ```

3. **Installer les dépendances**
   ```sh
   pip install -r docs/requirements.txt
   ```

4. **Lancer l'application Streamlit**
   ```sh
   streamlit run wheather_electricity.py
   ```

5. **Explorer le notebook d'analyse**
   Ouvrir `script_analyse.ipynb` avec Jupyter Notebook :
   ```sh
   jupyter notebook script_analyse.ipynb
   ```

6. **Exécuter le traitement des données API**
   Ouvrir `traitement.ipynb` avec Jupyter Notebook :
   ```sh
   jupyter notebook analyse_avec_API.ipynb
   ```

## Fonctionnalités

### 1. Prétraitement et analyse des données
- Chargement et nettoyage des données météorologiques et de consommation électrique.
- Regroupement des données par période et agrégation des mesures.

### 2. Application Streamlit
- **Onglet "Impact de météo sur Consommation d'électricité"** : Visualisation des relations entre température, pression, précipitations et consommation.
- **Onglet "Données météorologiques"** : Analyse des tendances météorologiques sur la période étudiée.

### 3. Analyse des données météorologiques via API
- Extraction massive de données météorologiques via une API.
- Traitement et mise en forme des données pour une analyse approfondie.

## Configuration de `.gitignore`
Le fichier `.gitignore` empêche l'ajout de certains fichiers au dépôt Git. Voici son contenu :
```
# Environnement virtuel
bigdata_env/

```

