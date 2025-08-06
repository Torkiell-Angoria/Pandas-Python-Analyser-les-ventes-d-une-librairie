# 📦 Projet Bottleneck – Analyse des ventes et gestion des stocks
## 🧑‍🎓 Présentation du projet

Ce projet a été réalisé dans le cadre de ma formation en data analyse. L'objectif était d'accompagner l’entreprise Bottleneck, spécialisée dans la vente de produits en ligne, dans l’exploitation de ses données commerciales.

Les outils actuellement utilisés par l’entreprise sont artisanaux, ce qui complique le suivi des stocks et l’analyse des ventes. Ce projet a donc été divisé en deux grandes phases :
Phase 1 – Agrégation et nettoyage des données
Phase 2 – Analyse stratégique pour le comité de direction (CODIR)

Le travail accompli ici servira de base au futur projet de visualisation de données de l’entreprise.

## 🎯 Objectifs pédagogiques et métiers

Savoir traiter des données provenant de plusieurs sources (ERP, site e-commerce, table de liaison).
Être capable de nettoyer, fiabiliser et structurer une base de données.
Réaliser une analyse commerciale complète en vue de soutenir une prise de décision stratégique.
Appliquer les principes de conformité au RGPD lors du traitement de données.
Apprendre à synthétiser ses résultats pour un public non technique (CODIR).

## 🧰 Outils et langages utilisés
Python (Jupyter Notebook) pour le traitement et l’analyse des données
Pandas, NumPy pour la manipulation des datasets
Seaborn, Matplotlib pour la création de graphiques
Scipy, Statsmodels pour l’analyse statistique
Git/GitHub pour le versioning
Excel / CSV pour les fichiers source
Méthodes statistiques : Z-score, IQR, corrélation, Pareto

## 🗃️ Sources de données utilisées
Export ERP : contient les informations de stock, prix de vente, état du stock, etc.
Export du site web (WordPress) : contient les ventes du 1er au 31 octobre, descriptions, quantités vendues…
Table de liaison des produits : permet de relier les références entre les deux sources. Mise à jour récemment par le stagiaire.

#### 🧪 Phase 1 – Nettoyage et structuration
Étapes réalisées :
Fusion des trois fichiers via la table de correspondance des références.
Détection de 8 types d’erreurs, dont :
    Doublons et incohérences de format
    Références absentes d’une des bases
    Erreurs de type (nombres stockés en texte)
    Incohérences dans les valeurs de prix
    Données manquantes ou aberrantes
    Problèmes d'arrondis et de calcul automatique

Propositions d’amélioration :
    Standardiser les formats de référence produit entre ERP et WordPress
    Mettre en place des règles de validation à la saisie dans le système ERP
    Créer une base de produits maîtres avec identifiants uniques
    Automatiser les contrôles de cohérence via des scripts Python

#### 📊 Phase 2 – Analyse stratégique

L’analyse a été pensée pour répondre aux attentes du comité de direction de manière claire et synthétique.
###### 🔹 1. Calculs de chiffre d’affaires
Chiffre d’affaires par produit

Chiffre d’affaires total de la période
Visualisation des meilleures ventes

###### 🔹 2. Analyse des meilleures références
Application du principe Pareto (20/80) pour repérer les produits les plus stratégiques
Recommandations sur les références à suivre ou à déréférencer

###### 🔹 3. Détection des valeurs aberrantes
Analyse via Z-score et écart interquartile (IQR)
Boxplots pour identifier les produits avec des prix incohérents
 Mise en lumière de potentielles erreurs de prix de vente

###### 🔹 4. Rotation des stocks
Calcul du nombre de mois de stock restants
Identification des stocks dormants ou sous tension
Analyse croisée avec les ventes pour optimiser le réapprovisionnement

###### 🔹 5. Analyse de corrélation
Étude des relations entre :
    prix et ventes
    marge et quantité en stock
    prix d’achat et prix de vente
    Utilisation de la matrice de corrélation pour visualiser les dépendances

## 🔐 Respect du RGPD
Aucune donnée personnelle traitée dans le cadre de ce projet
Nettoyage préalable pour retirer tout champ nominatif
Propositions pour la pseudonymisation ou suppression automatique des champs sensibles
Démarche documentée dans un fichier de conformité RGPD (dans le dossier /report/)

## 🧾 Résultats livrés
Base de données propre et exploitable
Synthèse claire pour présentation CODIR
Graphiques en haute qualité exportables
Fichier .csv avec les métriques clés
Recommandations concrètes pour l’avenir

## 🧠 Compétences développées

Traitement de données multi-source avec jointures complexes
Nettoyage avancé et gestion des anomalies de données
Analyse de la performance commerciale d’un catalogue produit
Communication des résultats à un public non technique
Formalisation de recommandations et respect du cadre légal (RGPD)
