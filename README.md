# Analyse statistique des défaillances récurrentes dans les réseaux électriques

## 📌 Présentation du projet

Ce dépôt présente une étude statistique des **indisponibilités récurrentes de liaisons électriques**, réalisée dans le cadre d’un stage de Master en Statistique Appliquée.

L’objectif est de modéliser et comprendre l’occurrence des pannes dans les infrastructures de transport d’électricité à l’aide de méthodes statistiques rigoureuses, depuis le nettoyage des données jusqu’à la modélisation avancée des événements récurrents.

Le projet met en œuvre :

* Nettoyage et préparation de données
* Analyse exploratoire et visualisation
* Estimation non paramétrique de processus d’événements récurrents
* Modélisation semi-paramétrique
* Interprétation statistique dans un contexte industriel

L’accent est mis sur la **rigueur mathématique**, la reproductibilité et la pertinence applicative.

---

## ⚡ Contexte industriel

Les réseaux de transport d’électricité subissent des indisponibilités répétées dues à des défauts techniques, conditions climatiques ou opérations de maintenance.

Comprendre ces défaillances permet de :

* améliorer la fiabilité du réseau
* optimiser la maintenance
* réduire les risques opérationnels

Chaque panne est modélisée comme un **événement récurrent** observé sur une liaison électrique au cours du temps.

---

## 📊 Description des données

Le jeu de données contient des enregistrements d’indisponibilités avec :

* Identifiant de la liaison
* Dates de début et fin d’indisponibilité
* Durée de panne
* Caractéristiques de la liaison :

  * Longueur
  * Âge
  * Niveau de tension

Certaines informations industrielles ont été anonymisées.

---

## 🧹 Pipeline de traitement des données

L’analyse suit les étapes suivantes :

1. **Nettoyage**

   * Conversion des dates
   * Suppression des durées invalides
   * Gestion des valeurs manquantes

2. **Construction des variables**

   * Format événements récurrents
   * Catégorisation du niveau de tension

3. **Analyse exploratoire**

   * Nombre de pannes par niveau de tension
   * Distribution des durées
   * Évolution temporelle des défaillances

---

## 📈 Méthodologie statistique

### 1. Estimation non paramétrique

On estime la **fonction cumulative moyenne (Mean Cumulative Function – MCF)** des événements récurrents.

Cette approche permet :

* d’estimer le nombre moyen de pannes dans le temps
* de comparer différents niveaux de tension
* d’analyser la fiabilité du réseau

L’estimateur est lié à l’estimateur de Nelson–Aalen pour processus de comptage.

---

### 2. Modélisation semi-paramétrique

On utilise des modèles de régression pour événements récurrents de type Cox afin d’évaluer l’effet de variables explicatives :

* Longueur de la liaison
* Âge
* Niveau de tension

Ces modèles permettent de quantifier l’influence des caractéristiques des ouvrages sur l’intensité des pannes.

---

## 📊 Résultats obtenus

Les analyses produisent notamment :

* Courbes MCF par niveau de tension
* Estimation des effets des covariables
* Interprétation statistique de la fiabilité des infrastructures

Les figures sont entièrement reproductibles à partir des scripts R fournis.

---

## 🛠 Outils utilisés

Analyse réalisée en **R**, avec :

* `dplyr` – manipulation de données
* `ggplot2` – visualisation
* `reda` – estimation non paramétrique
* `reReg` – régression pour événements récurrents
* `survival` – cadre processus de comptage

---

## 📂 Structure du dépôt

```id="fd83kx"
data/        → jeu de données exemple
scripts/     → script principal d’analyse
figures/     → graphiques générés
README.md    → description du projet
```

---

## 🎯 Compétences mises en valeur

Ce projet illustre des compétences en :

* Statistique des événements récurrents
* Analyse de fiabilité
* Analyse de survie
* Nettoyage et visualisation de données
* Reproductibilité scientifique
* Application des mathématiques à l’industrie

---

## 📖 Références

* Lawless, J.F. & Nadeau, C. (1993). *Some Simple Robust Methods for the Analysis of Recurrent Events*.
* Nelson, W. (1995). *Confidence limits for recurrence data*.

---

## 👤 Auteur

Étudiant en Master 2 Mathématiques Appliquées – Statistique & Data Science.
Recherche d’opportunités en :

* Data Science
* Modélisation statistique
* Fiabilité des systèmes

N’hésitez pas à me contacter via LinkedIn ou GitHub.

---

## ⭐ Remarque

Ce dépôt contient une **version représentative** du travail réalisé en stage.
Certaines données et analyses complètes ne peuvent être publiées pour des raisons de confidentialité industrielle.
