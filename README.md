# Optimisation de la Planification des Voyages - Compagnie LK (Togo)
## Présentation du Projet
Ce projet a pour objectif d'améliorer l'efficacité opérationnelle de la compagnie de transport LK, qui assure des liaisons régulières entre les principales villes du Togo (Lomé, Kara, Sokodé, Atakpamé, Dapaong, Tsévié).

Face à des problématiques de retards, de gestion de flotte et de baisse de satisfaction client, cette étude propose une approche basée sur la science des données pour optimiser la planification des trajets et prédire la qualité de service.

## Problématique et Objectifs
La direction de LK souhaite exploiter ses données historiques (2 000 à 10 000 trajets) pour répondre aux défis suivants:


Analyse des retards : Identifier les facteurs causant les retards fréquents.


Gestion de la capacité : Éviter la surcharge ou la sous-utilisation des bus.


Optimisation des coûts : Réduire la consommation de carburant sur certains axes.


Satisfaction client : Prédire les niveaux de satisfaction pour améliorer le service.

## Données Utilisées
Le jeu de données comprend des informations détaillées sur les trajets réalisés:


Caractéristiques du trajet : Villes de départ/arrivée, distance, durée prévue, état des routes.


Informations bus : Type de bus (Standard, Climatisé, VIP), capacité, nombre de passagers.


Indicateurs de performance : Retard observé, consommation de carburant, prix du billet.


Cible : Satisfaction client (score de 1 à 5).

## Méthodologie & Pipeline Technique
Le projet implémente un pipeline de prétraitement robuste via scikit-learn pour garantir la reproductibilité entre les phases d'entraînement et de test:

Nettoyage des données :

Imputation des valeurs manquantes (SimpleImputer).

Correction des incohérences (ex: nombre de passagers supérieur à la capacité).

Feature Engineering :

Calcul du taux de remplissage des bus.

Calcul du retard par kilomètre ou par heure.

Transformation des variables :

Encodage One-Hot pour les variables catégorielles (villes, types de bus, etc.).

Mise à l'échelle (StandardScaler) des variables numériques.

Modélisation :

Comparaison de modèles : Régression Logistique et Random Forest.

## Résultats
Le modèle final basé sur l'algorithme Random Forest a démontré une excellente capacité prédictive :


ROC AUC Score : 0.885

Le modèle permet d'identifier avec précision les trajets à haut risque de retard ou d'inefficacité, offrant ainsi un outil d'aide à la décision précieux pour la planification de LK.
