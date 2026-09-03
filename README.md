# Analyse du circuit professionnel de Tennis

Ce projet propose un état des lieux du tennis professionnel masculin en simple afin de comprendre et visualiser ses évolutions sur environ 30 ans.

## Table des matières

- [Présentation du projet](#aperçu-projet)
- [Problématique](#problématique)
- [Objectifs](#objectifs)
- [Public cible](#public-cible)
- [Axes d'analyse](#axes-d'analyse)
- [Sources de données](#sources-de-données)
- [Préparation des données](#préparation-des-données)
- [Gestion des valeurs manquantes](#gestion-des-valeurs-manquantes)
- [Enrichissement des données](#enrichissement-des-données)
- [Visualisation](#visualisation)
- [Stack technique](#stack-technique)
- [Compétences développées](#compétences-développées)

## Présentation du projet

Ce projet a vu le jour lors d'un projet de la formation de Data Analyst d'Open Classrooms, le sujet était libre et l'approfondissement de celui-ci également. L'objectif était de réaliser toutes les étapes de réponse à un besoin. Dans mon cas, le public cible était un journaliste sportif qui avait besoin d'écrire un article sur l'évolution du tennis.

Lorsque le sujet a été trouvé, il a fallu effectuer la récupération de données, le nettoyage/traitement, le croisement, la détection de KPI importante et la représentation sous forme de graphique de ces derniers.

L'analyse porte à la fois sur les joueurs, les tournois, les surfaces, les classements, les nationalités et les statistiques de matchs.

--

## Problématique

Comment le tennis professionnel masculin a-t-il évolué au cours des dernières décennies, à travers :

- le profil physique et identitaire des joueurs
- le contenu des tournois et des différents circuits
- les classements et les périodes de domination
- les victoires et les nationalités représentées
- les statistiques individuelles des joueurs

## Objectifs

- construire un état des lieux historique du tennis professionnel masculin
- comparer les différentes époques
- analyser l'évolution des joueurs et des compétitions
- identifier les joueurs et nationalités les plus marquants
- étudier les performances statistiques en match
- créer des visualisations statiques et interactives

## Public cible

Le projet s'adresse principalement :

- aux analystes sportifs
- aux journalistes spécialisés
- aux passionnés de tennis
- aux personnes souhaitant explorer l'histoire récente du tennis professionnel

## Axes d'analyse

### 1. Profils des joueurs

Analyse de l'évolution :

- de l'âge
- de la taille
- de la main dominante
- des nationalités
- de la représentation des pays

### 2. Tournois et surfaces

Analyse :

- des circuits professionnels
- des surfaces
- des types de tournois
- du volume de matchs
- de l'évolution du contenu des compétitions

### 3. Classements

Analyse :

- de l'évolution des rankings
- des meilleurs joueurs par époque
- de la stabilité du Top 10
- des périodes de domination

### 4. Victoires et palmarès

Analyse :

- des joueurs les plus titrés
- des nationalités les plus victorieuses
- des titres par circuit
- des titres par surface

### 5. Statistiques des joueurs

Analyse des performances en match :

- aces
- doubles fautes
- premières balles
- jeux de service gagnés
- balles de break
- performances au service et au retour

## Sources de données

Les données principales proviennent du [dépôt GitHub de Jeff Sackmann](https://github.com/JeffSackmann/tennis_MatchChartingProject).

Elles comprennent notamment :

- des fichiers de matchs par année et par circuit
- un fichier regroupant les joueurs
- des fichiers de classements par période

Des sources complémentaires ont également été utilisées pour enrichir les informations manquantes.

## Préparation des données

Les principales étapes sont :

1. Importation automatique des fichiers
2. Concaténation des fichiers annuels
3. Contrôle du nombre de lignes
4. Création d'identifiants uniques
5. Détection et traitement des doublons
6. Analyse des valeurs manquantes
7. Nettoyage des données
8. Enrichissement des données joueurs
9. Préparation des tables finales pour l'analyse sous forme de graphique

## Gestion des valeurs manquantes

Les données historiques comportent davantage de valeurs manquantes dans les périodes anciennes, notamment avant 2009.

Ces valeurs n'ont pas systématiquement été supprimées, car les conserver permet de comparer les différentes époques.

Les méthodes utilisées sont :

- enrichissement manuel - rapprochement avec d'autres jeux de données
- enrichissement automatique - scraping de Wikipédia
- filtrage des joueurs n'ayant pas participé à la période étudiée
- exclusion du reste des valeurs manquantes lorsque leur remplacement n'est pas suffisamment fiable ou possible

## Enrichissement des données

Un script Python utilisant notamment `requests` et `BeautifulSoup` a été développé afin de récupérer des informations complémentaires sur Wikipédia.

Les étapes comprennent :

- récupération des pages
- extraction des informations
- nettoyage des textes
- normalisation des valeurs
- rapprochement avec les identifiants joueurs
- contrôle des résultats

L'utilisation de sources ATP Tour et ITF Tennis aurait également pu compléter certaines informations. Cependant, leur automatisation aurait nécessité une prise en main de Selenium, ce qui n'a pas pu être réalisé dans le temps disponible.

## Visualisation

Les graphiques ont d'abord été développés de manière statique dans Jupyter Notebook.

Les données préparées ont ensuite été exportées afin de construire des vues interactives dans Tableau Public, puis plusieurs dashboards organisés par thématique.

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/bf9ec81e-adfb-4e69-b35a-56d2dbadb5d1" />

## Stack technique

| **Domaines** | **Technologies** |
|---|---|
| **Conception** | `Blueprint`, `mockups` |
| **Langage** | `Python` |
| **Packages** | `Pandas`, `NumPy`, `Requests`, `BeautifulSoup`, `Matplotlib`, `Seaborn`, `OpenPyXL` |
| **Collecte de données** | `Fichiers CSV d'un GitHub`, `scraping Wikipédia`, `Sites spécialisés` |
| **Outil de développement** | `Jupyter Notebook` |
| **Package - Visualisation statique** | `Matplotlib`, `Seaborn` |
| **Visualisation dynamique** | `Tableau Public` |

## Compétences développées

Ce projet m'a permis de développer et de mettre en œuvre mes compétences dans les domaines suivants.

_Cadrage et conception :_

- analyse et formalisation d’un besoin métier
- identification des utilisateurs et des objectifs d’analyse
- création d’un blueprint fonctionnel
- conception de mockups
- définition d’indicateurs clés et d’axes d’analyse

_Traitement de la donnée :_

- recherche de sources de données adaptées
- nettoyage des données
- enrichissement des données + utilisation de scrapping
- préparation de données pour la visualisation
- création des visualisation statique sous Python et dynamique sous Tableau Public

_Documentation et gestion de projet :_

- documentation des sources et des traitements
- explication des choix méthodologiques
- vulgarisation des analyses techniques
- organisation d’un projet data de bout en bout
