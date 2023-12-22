# Projet-NLP_Detection-des-Fake-News

# 1. Introduction
Dans un monde où les réseaux sociaux jouent un rôle central dans la diffusion de l'actualité et où l'accès à l'information est de plus en plus rapide, la propagation de fausses informations représente un défi majeur. Les fake news, souvent créées dans le but de tromper le public, peuvent avoir des répercussions graves sur la société. La désinformation peut influencer les opinions, semer la confusion, et même menacer la stabilité sociale et politique. Ainsi, la détection de fake news est devenue une priorité afin de garantir l'intégrité de l'information et de préserver la confiance du public dans les sources d'actualités.
# 2. Objectif du Projet
Les attentes de ce projet incluent la création d'un modèle robuste capable de discerner avec précision les informations véridiques des fake news.
Les principales questions qui se posent à ce sujet comprennent :
- Comment les modèles basés sur le traitement du langage naturel peuvent-ils être adaptés pour détecter les fausses informations de manière efficace ?
- Quelles améliorations peuvent être apportées pour rendre les modèles de détection plus robustes face à l'évolution des tactiques de création de fake news ?
Dans notre projet, on a répondu à ces questions en fournissant des recommandations pratiques pour renforcer la détection de fake news dans un environnement d'information en constante évolution.

# 3. Modèles Utilisés
# Bert:
En premier lieu , on a initialement opté pour l'utilisation du modèle Bert (Bidirectional Encoder Representations from Transformers) précisément l’architecture de modèle basée sur lui, BertForSequenceClassification, qui est pré-entraîné pour la classification de séquences afin de générer un des résumés des articles de notre base de données.
# T5:
Cependant, après avoir évalué les résultats obtenus, nous avons constaté que cette approche ne satisfaisait pas nos exigences en termes de génération de résumés. En réponse à cela, nous avons décidé d'adopter une nouvelle approche en emplaçant le modèle BERT par le modèle T5 (Text-To-Text Transfer Transformer). Cette transition vers le modèle T5 vise à améliorer l'efficacité et la pertinence de notre travail dans le domaine de la détection de fake news.
En deuxième lieu, pour la détection de fake news, nous avons opté pour l'utilisation de deux modèles : RoBERTa (Robustly optimized BERT approach) et Mistral.
# RoBERTa (Robustly optimized BERT approach):
*RoBERTa est une amélioration de BERT(le modèle pré-entraîné qui excelle dans la compréhension contextuelle des mots dans une phrase) proposée par Facebook AI Research (FAIR).
*Contrairement à BERT, RoBERTa supprime certaines des tâches de pré-entraînement de BERT, comme la prédiction masquée, et utilise des hyperparamètres optimisés.
*RoBERTa est conçu pour être plus robuste et performant sur des tâches spécifiques, en particulier sur des jeux de données plus vastes et diversifiés.
# Mistral:
*Mistral a démontré une performance exceptionnelle dans des tâches de classification de texte,soulignant son efficacité dans la compréhension et la catégorisation de documents textuels.
*Comme RoBERTa, Mistral repose sur une architecture de transformer. Cette approche permet de capturer des représentations sémantiques complexes, facilitant ainsi la compréhension du contexte des mots dans un texte.
*Mistral a bénéficié d'un entraînement préalable sur des corpus textuels volumineux.
Cette immersion dans une grande quantité de données textuelles lui confère une compréhension approfondie du langage naturel et renforce ses capacités de traitement de l'information.
*Mistral se distingue par sa capacité à traiter de manière efficace des informations complexes. Cette caractéristique en fait un choix pertinent, notamment dans le contexte de la détection de fake news, où la compréhension fine et la lassification précise sont cruciales.
La décision d'utiliser RoBERTa et Mistral découle de leurs performances avérées dans des tâches similaires de classification de texte, reflétant leur capacité à saisir des nuances sémantiques subtiles. Ces deux modèles ont été sélectionnés pour exploiter leurs forces respectives et améliorer la précision de notre système de détection de fake news.
# 4. Jeu de Données
Pour notre projet de détection de fake news, le jeu de données qu’on a utilisé est celle du Fake News Challenge (FNC). Ce jeu de données se compose de deux principaux ensembles de données : les corps d'articles (`train_bodies.csv`, `test_bodies.csv`) et les déclarations (`train_stances.csv`, `test_stances_unlabeled.csv`).
