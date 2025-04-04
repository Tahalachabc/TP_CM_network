# TP_CM_network
#  Network Analysis for Information Retrieval  
**Projet M2 MALIA–MIASHS** — Université Lumière Lyon 2  
*Encadré par Julien Velcin – Laboratoire ERIC*  
 **Année universitaire : 2024–2025**

---

## Objectif du projet

Ce projet vise à explorer un corpus scientifique (extrait de DBLP) à travers une double approche **textuelle et structurée**, en combinant :

- **Traitement automatique des langues (TAL)**  
- **Analyse de réseaux (graph mining)**
- **Apprentissage supervisé**  
- **Visualisation interactive et réduction de dimension**

Le tout appliqué à des tâches de **recherche d'information**, **classification**, et **recommandation d'auteurs**.

---

## Structure du travail

Le projet est structuré en 4 TPs, réalisés de manière progressive.

###  TP1 – Chargement et prétraitement
- Lecture d'un corpus JSON (format DBLP)
- Nettoyage : suppression des valeurs manquantes, extraction des colonnes utiles
- Analyse exploratoire : nombre d'articles, distribution des citations

### TP2 – Indexation sémantique
- Nettoyage linguistique avec **spaCy** : lemmatisation, stopwords
- Construction de matrices TF / TF-IDF
- Recherche de documents similaires par **cosine similarity**
- Visualisation des termes importants (poids TF-IDF)

### TP3 – Analyse de graphe
- Construction du **graphe de citations**
- Extraction d’un **sous-graphe k-core** ou de la **composante géante**
- Application du clustering (Louvain, spectral)
- **Node2Vec** pour apprendre des représentations vectorielles des articles
- Visualisation en 2D des clusters d’articles

### TP4 – Approfondissements

#### 8.1 Classification supervisée
- 3 approches testées :
  - Méthode naïve (par mots-clés)
  - **Random Forest** sur vecteurs TF-IDF
  - **GCN (Graph Convolutional Network)** avec PyTorch Geometric
- Recatégorisation automatique en **8 classes thématiques**
- Équilibrage des données + évaluation via F1-score et matrice de confusion

#### 🔸 8.2 Identification d’auteurs
- Représentation de chaque auteur par la **moyenne des embeddings Node2Vec** de ses articles
- Recherche d’auteur probable à partir d’un texte
- Évaluation via le **rang moyen**, **top-1** et **top-5 accuracy**
- **Projection 2D** des auteurs avec PCA (Matplotlib)
> *(La version interactive avec Plotly a été envisagée mais non implémentée)*

---

## Points forts

-  Pipeline complet texte + graphe
- Application de modèles avancés (GCN, Node2Vec)
- Évaluation rigoureuse : classification + recommandation
- Visualisations claires et structurées
- Capacité à adapter les traitements selon la qualité des données

---

## Fichiers associés

- `CM_network_TPS.ipynb` : notebook principal
- `TP1.pdf` à `TP4.pdf` : énoncés du projet
- `README.md` : description du projet (ce fichier)

---

## Réalisé par

- **Lachab Taha**  
- **Renac Alexandre**  
🎓 Master 2 **MIASHS**  
Université Lumière Lyon 2

---
