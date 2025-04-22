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

## Considérations éthiques
- Transparence et explicabilité des résultats
- Identification de biais potentiels dans les données et le modèle

## Conclusion
Ce projet met en pratique des compétences avancées en NLP, deep learning, interprétabilité et déploiement embarqué. Nous avons non seulement conçu un modèle prédictif performant, mais aussi veillé à sa transparence, à son impact environnemental et à sa portabilité vers des plateformes énergétiquement contraintes.

## Licence
Ce projet est distribué sous la licence MIT.

