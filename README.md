# Détection de Contenu Toxique

Ce projet vise à détecter automatiquement différents types de commentaires toxiques en ligne (menaces, obscénités, insultes, etc.) à l’aide de techniques avancées de traitement du langage naturel (NLP).

## Objectifs
- Identifier plusieurs types de toxicité (toxic, severe toxic, obscene, threat, insult, identity hate).
- Améliorer les performances des modèles existants en combinant différentes approches.
- Fournir un pipeline modulaire pour une intégration facile dans des systèmes de modération.

## Méthodologie
1. **Préparation des données** :
   - Nettoyage des textes (suppression des URL, ponctuation, etc.).
   - Représentation des données avec TF-IDF et embeddings GloVe.
2. **Modélisation** :
   - TF-IDF avec régression logistique.
   - LSTM avec embeddings GloVe.
   - Combinaison des prédictions pour améliorer la robustesse.
3. **Évaluation** :
   - Utilisation des métriques ROC AUC et matrices de confusion.

## Résultats
- **TF-IDF** : ROC AUC moyen de 0.9112.
- **GloVe** : ROC AUC moyen de 0.9160.
- **Combinaison des modèles** : ROC AUC moyen de 0.9194.
- Meilleures performances sur les classes "toxic" et "obscene", mais des difficultés pour les classes "threat" et "identity hate".

## Outils et Technologies
- **Python** : Langage principal.
- **Bibliothèques** :
  - Scikit-learn : Modèles TF-IDF.
  - TensorFlow/Keras : Modèles LSTM.
  - Pandas et NumPy : Manipulation des données.
  - Matplotlib/Seaborn : Visualisation.
- **Environnement** : Google Colab avec support GPU.

## Limitations
- Déséquilibre des classes dans le dataset.
- Limitations matérielles empêchant l’utilisation de modèles plus complexes comme BERT.

## Perspectives
- Amélioration du dataset avec des données annotées supplémentaires.
- Optimisation des ressources pour entraîner des modèles contextuels (e.g., BERT, RoBERTa).
- Développement d’un système personnalisable permettant aux utilisateurs de prioriser certains types de toxicité.

## Conclusion
Ce projet démontre qu’une combinaison de techniques classiques et avancées en NLP permet de détecter efficacement différents types de commentaires toxiques, tout en offrant une base solide pour des améliorations futures.
