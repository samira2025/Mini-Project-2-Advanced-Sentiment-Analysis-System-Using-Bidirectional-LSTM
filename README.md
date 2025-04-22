# Mini-Project-2-Advanced-Sentiment-Analysis-System-Using-RNNs

## Introduction
Dans ce mini-projet, nous avons conçu un système avancé d'analyse de sentiment appliqué à des critiques de films. Contrairement à une approche classique de type régression logistique, nous avons utilisé un modèle de deep learning basé sur des couches Bidirectional LSTM. Le projet intègre également des techniques d'interprétabilité (LIME et SHAP), une mesure de l'empreinte carbone (CodeCarbon), ainsi qu'une conversion du modèle vers TensorFlow Lite pour le déploiement sur systèmes embarqués.

## Objectifs
1. **Préparation des données** : Chargement et exploration du jeu de données IMDb.
2. **Nettoyage du texte** : Suppression des balises HTML, ponctuation et mots vides.
3. **Vectorisation** : Tokenisation, indexation et padding des critiques.
4. **Conception du modèle** : Réseau RNN à base de LSTM bidirectionnels.
5. **Entraînement et validation** : Utilisation d'early stopping pour prévenir le sur-apprentissage.
6. **Analyse carbone** : Mesure de la consommation d'énergie avec CodeCarbon.
7. **Explicabilité** : Visualisation de l'impact des mots avec SHAP et LIME.
8. **Optimisation** : Ajustement des hyperparamètres (dropout, batch size, learning rate).
9. **Déploiement embarqué** : Conversion vers TensorFlow Lite, analyse des performances.
10. **Documentation & publication** : Préparation du repo GitHub, choix de la licence open-source.

## Données
- Le jeu de données IMDb contient 50 000 critiques labellisées.
- Source : [https://ai.stanford.edu/~amaas/data/sentiment/](https://ai.stanford.edu/~amaas/data/sentiment/)

## Prétraitement
- Conversion en minuscules, suppression des balises HTML
- Filtrage de la ponctuation et des mots vides, en gardant certains mots clés (ex: "not")
- Padding des séquences à une longueur fixe (200)

## Conception et entraînement du modèle
- Deux couches Bidirectional LSTM
- Dropout pour réduire le sur-apprentissage
- Dense avec activation sigmoid pour classification binaire
- Optimiseur Adam, early stopping sur la validation loss

## Evaluation et performances
- Accuracy élevée sur l'ensemble de test
- Bon pouvoir de généralisation sur des critiques personnalisées

## Interprétation des résultats
- **LIME** : mise en évidence des mots influents localement
- **SHAP** : visualisation des contributions positives/négatives de chaque mot

## Empreinte carbone
- Intégration de CodeCarbon pendant l'entraînement
- Estimation de l'énergie consommée et des émissions de CO2

## Déploiement sur systèmes embarqués
- Conversion du modèle vers le format `.tflite`
- Activation du Flex Delegate pour gérer les TensorList
- Comparaison taille, temps d'inférence et précision avant/après conversion

## Documentation et publication
- Rédaction d'un README complet (objectifs, instructions, analyse carbone, explications SHAP/LIME)
- Utilisation d'une licence open-source (MIT)
- Protocole de publication : issues, pull requests, validation par tests

## Responsabilités liées à la publication du code
La publication du code source implique des responsabilités importantes en matière de transparence, de maintenance et d'accessibilité.

Le code fourni a été inspiré et tiré en partie du cours **GEI1092 - Techniques d'intelligence artificielle** de l'Université du Québec à Trois-Rivières. Ce cours lui-même s'appuie sur plusieurs ressources académiques et ouvrages de référence en apprentissage automatique et intelligence artificielle, notamment :

1. **Raschka Sebastian, Vahid Mirjalili** – *Machine Learning and Deep Learning with Python, scikit-learn, and TensorFlow 2*, 3ᵉ édition, Packt Publishing, 2019.  
2. **Ian Goodfellow, Yoshua Bengio, Aaron Courville** – *Deep Learning*, The MIT Press, novembre 2016.  
3. **Raschka Sebastian** – *Build a Large Language Model*, 1ʳᵉ édition, Manning, octobre 2024.  
4. **Denis Rothman** – *Hands-On Explainable AI (XAI) with Python*, 1ʳᵉ édition, Packt Publishing, juillet 2020.  
5. **Serg Masís** – *Interpretable Machine Learning with Python - Second Edition*, Packt Publishing, octobre 2023.  
6. **CodeCarbon** : [https://mlco2.github.io/codecarbon/](https://mlco2.github.io/codecarbon/)  
7. **K. Lottick et al.** – *Energy Usage Reports: Environmental awareness as part of algorithmic accountability*, arXiv:1911.08354v2, 16 décembre 2019.  
8. **Peter Wentworth, Jeffrey Elkner, Allen B. Downey, Chris Meyers** – *How to Think Like a Computer Scientist: Learning with Python 3*, 3ᵉ édition, février 2019.  

Les données utilisées dans ce projet proviennent du jeu de données IMDb, qui est open source. L'ensemble du code et des modèles est développé dans un esprit d'éthique et de responsabilité envers la communauté scientifique et les utilisateurs finaux.

## Installation et exécution
1. Cloner le dépôt :  
```bash
git clone https://github.com/D0ntMindMe/Mini-Project-1-Building-a-Sentiment-Analysis-System-for-Movie-Reviews-
cd sentiment-analysis-project
```
2. Installer les dépendances :  
```bash
pip install -r requirements.txt
```
3. Exécuter le script principal :  
```bash
python main.py
```

## Considérations éthiques
- Transparence et explicabilité des résultats
- Identification de biais potentiels dans les données et le modèle

## Conclusion
Ce projet met en pratique des compétences avancées en NLP, deep learning, interprétabilité et déploiement embarqué. Nous avons non seulement conçu un modèle prédictif performant, mais aussi veillé à sa transparence, à son impact environnemental et à sa portabilité vers des plateformes énergétiquement contraintes.

## Licence
Ce projet est distribué sous la licence MIT.
