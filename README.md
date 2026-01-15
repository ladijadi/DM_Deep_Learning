# DM Deep Learning – Prédiction du risque de cancer du sein

## Contexte

Ce projet a été réalisé dans le cadre du **DM de Deep Learning** (IDMC).  
L’objectif est de mettre en œuvre l’ensemble des étapes d’un projet d’intelligence artificielle appliqué à un cas réel.

Le cas d’usage concerne un **cabinet médical** souhaitant améliorer ses recommandations de dépistage du cancer du sein en prenant en compte plusieurs facteurs de risque, au-delà du critère de l’âge.

## Données

Le projet utilise le dataset public **tarekmasryo/cancer-risk-factors** (HuggingFace).

- Le dataset contient plusieurs types de cancers.
- Pour répondre au cas d’usage, seules les données liées au **cancer du sein** ont été conservées.
- La variable cible correspond au niveau de risque :
  - Low
  - Medium
  - High

Le jeu de données est fortement **déséquilibré**, en particulier pour la classe *High*.

## Méthodologie

Le projet suit les étapes du cycle **CRISP** :

1. Compréhension du besoin métier  
2. Compréhension et exploration des données  
3. Préparation des données (nettoyage, encodage, normalisation)  
4. Modélisation  
5. Évaluation des performances  
6. Interprétation des résultats  
7. Conclusion et recommandations  

Chaque étape est expliquée directement dans les notebooks à l’aide de blocs de texte.

## Modèles testés

Trois approches ont été étudiées :

- **Approche 1** : MLP (Multi-Layer Perceptron) avec pondération des classes (`class_weight`)
- **Approche 2** : Balanced Random Forest
- **Approche 3** : Balanced Random Forest avec seuil de sécurité (priorité à la détection des cas à haut risque)

L’objectif n’est pas uniquement de maximiser l’accuracy globale, mais d’analyser les compromis entre performance globale et détection des classes rares.

## Structure du dépôt

├── DM_deepleanring.ipynb # Notebook principal (MLP + analyse complète)

├── DM_deeplearning_models.ipynb # Notebook complémentaire (modèles équilibrés)

├── README.md



## Outils utilisés

- Python  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- imbalanced-learn  
- Matplotlib  

## Auteur

**Khady Diagne**  
Étudiante en Master 2 Science des données - IDMC  
DM Deep Learning - 2025

