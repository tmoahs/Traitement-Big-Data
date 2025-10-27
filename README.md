# Projet 9 : Réalisez un traitement dans un environnement Big Data sur le Cloud

### Objectif & Résultat Principal

Mise en place d'un pipeline de feature engineering scalable sur **AWS** pour un projet AgriTech ("Fruits!"). Le processus, orchestré sur un cluster **EMR avec PySpark**, charge les images depuis **S3** et applique un transfer learning (**MobileNetV2**) via **UDF Pandas**, après **broadcast** des poids du modèle. Une **PCA (PySpark ML)** a ensuite réduit la dimension des features à 100 composantes, optimisant le stockage avant sauvegarde au format **Parquet** sur S3.

---

Ce projet, le neuvième du parcours Data Scientist d'OpenClassrooms, consiste à migrer un processus de traitement de données (images) d'un environnement local vers une architecture cloud Big Data, en prévision d'une augmentation massive du volume de données.

### Contexte

La start-up AgriTech "Fruits!" souhaite développer des robots cueilleurs intelligents. La première étape est de lancer une application mobile permettant au grand public de prendre en photo un fruit pour l'identifier. Cette application servira à construire le moteur de classification et, surtout, à établir l'architecture Big Data nécessaire pour supporter la croissance future.

Le volume de données images devant augmenter très rapidement, ma mission est de bâtir les fondations d'un pipeline de feature engineering scalable sur AWS.

### Missions

* **Mise en place d'un cluster Big Data** : Configuration et déploiement d'un cluster **AWS EMR** (Elastic MapReduce) opérationnel.
* **Intégration du stockage Cloud** : Lecture et écriture des données (images brutes et features traitées) directement depuis et vers **AWS S3**.
* **Développement d'un pipeline PySpark** : Orchestration de l'ensemble du processus de traitement de données avec PySpark pour garantir la scalabilité.
* **Optimisation du Transfer Learning** : Implémentation du **broadcast** des poids du modèle (MobileNetV2) pour les diffuser efficacement à tous les nœuds du cluster.
* **Feature Engineering distribué** : Application du modèle de Deep Learning sur les images en utilisant des **Pandas UDF** pour un traitement parallélisé performant.
* **Réduction de Dimension** : Entraînement et application d'une **PCA** avec **PySpark ML** pour réduire la dimension des features (de 1280 à 100 composantes) et optimiser le stockage.
* **Optimisation du stockage** : Sauvegarde des features extraites au format **Parquet**, un format colonnaire optimisé pour les analyses Big Data.
* **Analyse critique et Recommandations** : Rédaction d'un retour sur l'architecture (coûts, performance, complexité EMR) et formulation de recommandations pour la mise en production (Auto Scaling, Spot Instances, monitoring).
* **Conformité RGPD** : Assurer que l'infrastructure AWS (région S3 et EMR) est configurée sur des serveurs situés en Europe.

### Compétences Développées

* **Big Data :** Traitement de données massives avec **PySpark** et son écosystème (**PySpark ML**).
* **Cloud Computing (AWS) :** Maîtrise de l'écosystème AWS pour la data : **AWS EMR** (cluster Spark managé) et **AWS S3** (stockage objet).
* **Architecture Pipeline :** Conception d'un pipeline de données complet, scalable et "cloud-native" (de S3 à S3).
* **Optimisation PySpark :** Utilisation de techniques avancées comme le **Broadcasting** (pour les poids du modèle) et les **Pandas UDF** (pour le traitement d'images) pour optimiser les performances et l'utilisation de la mémoire.
* **Machine Learning à grande échelle :** Application de techniques de Feature Engineering (Transfer Learning) et de réduction de dimension (PCA) dans un contexte distribué.
* **Gouvernance & Coûts :** Capacité à analyser de manière critique une solution cloud (coût vs performance) et à proposer des optimisations pour la production, tout en respectant les contraintes légales (RGPD).

### Outils et Librairies

* **Cloud :** AWS (EMR, S3)
* **Big Data :** Apache Spark (PySpark, PySpark ML)
* **Langage :** Python
* **ML / Deep Learning :** TensorFlow, Keras (pour MobileNetV2)
* **Manipulation de Données :** Pandas, NumPy
* **Traitement d'Image :** Pillow (PIL)
