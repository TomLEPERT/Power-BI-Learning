# Introduction

Dans cette série de quêtes, tu vas prendre en main l'outil Power BI Desktop, un puissant logiciel de Business Intelligence créé par Microsoft.

Lien de téléchargement de Power BI : https://www.microsoft.com/fr-FR/download/details.aspx?id=58494

## Objectifs

✅ Comprendre ce qu'est Power BI Desktop et son rôle dans la Business Intelligence
✅ Découvrir l'interface de Power BI Desktop et ses différentes fonctionnalités
✅ Maîtriser l'éditeur Power Query pour préparer efficacement tes données
✅ Créer ton premier rapport avec des visualisations interactives

## Sommaire

Introduction : Power BI Desktop, c'est quoi ?
    Définitions
L'interface Power BI Desktop
    Le ruban
    La zone de canevas
    La zone d'Onglets
    Le volet Filtres
    Le volet Visualisations
    Le volet Champs
    Les Vues
Power Query
    Qu'est ce qu'un ETL?
L'interface de Power Query
    Le Ruban
    Le volet Requêtes
    Le volet Paramètre de requête
    La Table de données
Challenge guidé
Challenge
    Critères de validation

## Introduction : Power BI Desktop, c'est quoi ?

### Définitions

#### Power BI Desktop

C'est une interface simple et intuitive de Business Intelligence conçue par Microsoft.
Elle permet de créer tes propres rapports et tableaux de bord interactifs à partir de diverses sources de données.

![Exemple de rapport](images\PBI_1_1.png)
Exemple de rapport créé à partir de la base de données SQL "toys and models"

#### Business Intelligence (BI)

Également connue sous le nom d'informatique décisionnelle, la BI vise à transformer des données brutes en informations pertinentes et exploitables. Son but est de permettre des prises de décisions éclairées sur la base de données fiables et à jour.

#### Le cycle de travail dans Power BI

Power BI Desktop fonctionne selon un processus en 5 étapes bien définies. Pour produire des rapports et tableaux de bord de qualité, il est essentiel de respecter chacune d'entre elles.

![Shémas de procéssus](images\PBI_1_2.png)

### L'interface Power BI Desktop

![Interface Power BI](images\PBI_1_3.png)

#### Le ruban

Situé dans la partie supérieure, le ruban contient les commandes et outils organisés par catégories dans différents onglets (Accueil, Insérer, Modélisation, etc.).

![Ruban](images\PBI_1_4.png)

> **Conseil pratique :**  
> Prends deux à trois minutes pour explorer les différents onglets du ruban (Accueil, Insérer, Modélisation, etc.) afin de te familiariser avec les possibilités offertes.

#### La zone de canevas

Présente au milieu de l'interface, c'est ici que tu vas créer et organiser les visualisations pour tes rapports. C'est ton espace de travail principal.

![Zone canvas](images\PBI_1_5.png)

#### La zone d'Onglets

Située dans la partie inférieure à gauche (en dessous de la zone de canevas), elle permet de sélectionner ou d'ajouter des pages au rapport, comme dans un classeur Excel.

![Zone onglet](images\PBI_1_6.png)

#### Le volet Filtres

Situé à droite du canevas, ce volet permet de filtrer les visualisations de données à différents niveaux (visualisation, page ou rapport).

![Filtres](images\PBI_1_7.png)

Avec cette imprécran, vous pouvez voir qu'il existe plusieurs possibilités de filtre. Nous les aborderons dans une autre quête.

> **Conseil pratique :**
> Le volet Filtres permet d'appliquer des filtres à trois niveaux différents:
    Filtres au niveau de la visualisation (appliqués à un visuel spécifique)
    Filtres au niveau de la page (appliqués à tous les visuels d'une page)
    Filtres au niveau du rapport (appliqués à toutes les pages du rapport)

#### Le volet Visualisations

Ce volet se divise en deux parties essentielles :
    La galerie de visualisations pour choisir le type de visuel

![Visualisation](images\PBI_1_8.png)

> **Conseil pratique :**  
> Survole chaque icône avec ta souris pour voir apparaître une info-bulle indiquant le nom du type de visualisation.

    Les champs de visualisation pour personnaliser ton visuel

![Champs](images\PBI_1_9.png)

#### Le volet Champs

Situé sur la droite de l'interface, ce volet affiche tous les champs disponibles dans tes sources de données connectées.
Pour créer des visualisations, tu peux faire glisser ces champs vers le canevas ou les zones du volet Visualisations.

![Volet champs](images\PBI_1_10.png)

#### Les Vues

Sur le côté gauche se trouvent les icônes correspondant aux trois vues principales de Power BI Desktop :

![Les vues](images\PBI_1_11.png)

    Vue Rapport : Pour créer et modifier des visualisations
    Vue Données : Pour examiner les données sous forme tabulaire
    Vue Modèle : Pour définir les relations entre les tables

La vue actuelle est indiquée par une barre verte sur le côté gauche de l'icône. Pour changer de vue, il suffit de cliquer sur l'icône correspondante.

### Power Query

La préparation des données s'effectue avec Power Query, l'ETL (Extract, Transform, Load) intégré à Power BI Desktop. Grâce à cet outil, tu vas réaliser les deux premières étapes du processus de création de rapport.

![Power query](images\PBI_1_12.png)

#### Qu'est ce qu'un ETL?

ETL(Extraire, Transformer, Charger) est un processus crucial en gestion de données qui se déroule en trois phases :

    1. Extract (Extraire) :

On collecte les données de diverses sources: bases de données, fichiers CSV, Excel, API web, etc.
Exemple: Extraire les données de ventes d'un système de caisse, les informations clients d'un CRM, etc.

    2. Transform (Transformer) :

On nettoie, formate, combine et enrichit les données pour les rendre exploitables.
Exemple: Standardiser les formats de date, éliminer les doublons, traiter les valeurs manquantes, etc.

    3. Load (Charger) :

On charge les données transformées dans un système cible prêt pour l'analyse.
Exemple: Charger les données nettoyées dans un modèle Power BI pour l'analyse ou la visualisation.

> **Avantages de l'ETL dans Power BI :**  
> Centralisation : Rassemble les données de multiples sources en un seul endroit
  Qualité : Assure la cohérence et la fiabilité des données
  Efficacité : Automatise le processus de préparation des données
  Traçabilité : Conserve l'historique des transformations appliquées

Commençons la pratique en nous connectant à une source de données web :

    Dans le ruban de Power BI Desktop, clique sur OBTENIR DES DONNEES.

![ETL1](images\PBI_1_13.png)

    Recherche et sélectionne Web dans la liste des sources disponibles, puis clique sur le bouton vert "SE CONNECTER".
    Une nouvelle fenêtre s'ouvre :

![ETL2](images\PBI_1_14.png)

Dans la fenêtre qui s'ouvre, saisis l'URL suivante : https://retirable.com/advice/lifestyle/best-worst-states-retire

Clique sur "OK" pour voir un aperçu du fichier, puis sur TRANSFORMER LES DONNÉES pour ouvrir l'éditeur Power Query (Les colonnes peuvent être différentes de celles qui sont affichées ci-dessous)

![ETL3](images\PBI_1_15.png)

### L'interface de Power Query

Tout comme Power BI Desktop, Power Query possède sa propre interface avec plusieurs zones importantes :

![Power query](images\PBI_1_16.png)

#### Le Ruban

![Ruban](images\PBI_1_17.png)

Il contient tous les outils de transformation disponibles, organisés par catégories dans différents onglets.

#### Le volet Requêtes

Il affiche toutes les sources de données connectées à ton rapport.

![Volet](images\PBI_1_18.png)

Note que dans notre cas, le fichier web importé se nomme "2309" et c'est l'unique requête pour l'instant.

#### Le volet Paramètre de requête

> **Ce volet est essentiel car il enregistre chaque étape de transformation appliquée à tes données. Il te permet de:**  
> Suivre l'historique complet des modifications
  Supprimer ou modifier des étapes spécifiques
  Comprendre la logique de transformation

![Parametre](images\PBI_1_19.png)

tu peux t'apercevoir que l’éditeur a déjà fait automatiquement deux modifications. Nous allons revenir sur ce sujet dans quelques instants.

#### La Table de données

Elle affiche un aperçu de tes données (par défaut les 1000 premières lignes) après application des transformations.

### Les bonnes pratiques en Power Query

> **Comme en programmation, il est essentiel de suivre certaines bonnes pratiques :**  
> Donner des noms explicites à tes requêtes
  Documenter les étapes de transformation complexes
  Organiser logiquement l'ordre des transformations

## Challenge guidé

Suis ces étapes pour transformer les données:

Clique-droit sur le nom de la requête dans le volet Requêtes et renomme-la en "State_for_retirement"

![Chall](images\PBI_1_20.png)

Pour mieux comprendre le fonctionnement de Power Query, supprime les étapes "En-têtes promus" et "Type modifié" en cliquant sur la croix à côté de chaque étape dans le volet Paramètres de requête. Observe attentivement les changements dans ta table.

![Chall](images\PBI_1_21.png)

Dans le ruban, va dans l'onglet TRANSFORMER et clique sur Utiliser la première ligne comme en-têtes

![Chall](images\PBI_1_22.png)

Tu remarqueras que deux nouvelles étapes se sont automatiquement créées : "En-têtes promus" et "Type modifié".

> **Pourquoi "Type modifié" est automatique ?**  
> Power Query analyse intelligemment le contenu de chaque colonne pour détecter automatiquement le type de données approprié (texte, nombre, date, etc.). Cette détection aide à assurer que tes données sont correctement formatées pour l'analyse.

## Challenge

En t'inspirant des étapes précédentes, connecte toi à une nouvelle source de données web : Liste des abréviations des États américains pour utiliser la table comme indiqué ci-dessous: https://en.wikipedia.org/wiki/List_of_U.S._state_and_territory_abbreviations

Ton objectif est d'extraire la table contenant les codes des États.
Suis ces 7 étapes de transformation :

    Renomme la requête en "Code"
    Supprime les premières lignes au-dessus de "United States of America" dans la colonne "Name"
    Utilise la première ligne pour les en-têtes de colonnes
    Renomme la colonne "US" en "Code" (clic-droit sur le nom de la colonne)
    Supprime toutes les colonnes sauf "United States of America", "Federal state" et "Code"
    Filtre la colonne "Federal State" pour ne conserver que les valeurs "State"
    Fusionne cette requête avec "State_for_Retirement" (en sélectionnant d'abord "State_for_Retirement")

Le résultat attendu doit ressembler à ceci (10 premières lignes de la requête "State_for_Retirement", avec la colonne "State" triée par ordre alphabétique) :

![Chall](images\PBI_1_23.png)

Une fois le résultat obtenu, ferme Power Query en cliquant sur "Appliquer et fermer" dans le ruban.

Crée les éléments suivants pour ton rapport :

    Titre principal : "What are the best states for retirement"
        Ruban > Accueil > Insérer > Zone de texte
        Utilise le volet Visualisations pour la mise en forme

    Carte géographique : "Top 10 Weather States"
        Sélectionne la visualisation Carte dans le volet Visualisations
        Fais glisser le champ "State" dans la zone Emplacement
        Personnalise la carte selon tes préférences

(Si la carte ne s'affiche pas, vas dans Fichier -> Options et paramètres -> Sécurité -> Coche "Visuels de carte et carte remplis. Et tu ne dois pas être connecté à un compte Power BI)

![Chall](images\PBI_1_24.png)

    Table de données : Top 10 des états selon différents critères
        Crée une table présentant le top 10 des états en fonction des conditions météorologiques (Weather), du coût de la vie (Affordability) et du classement général (Overall rank)
        
    Diagramme en barres : Top 10 des états selon le climat
        Crée un diagramme en barres montrant les dix premiers états en fonction du temps
        Applique un style cohérent (texte en bleu, police "Segoe UI")

Le résultat final devrait ressembler à ceci :
![Chall](images\PBI_1_25.png)

> **FÉLICITATIONS!**  
> Tu es désormais un nouvel utilisateur de Power BI! Tu as appris à:
    Te connecter à différentes sources de données
    Transformer et préparer tes données avec Power Query
    Créer des visualisations interactives pour analyser les informations
    N'oublie pas d'explorer l'interactivité entre tes visualisations en cliquant sur les différents éléments de ton rapport (points sur la carte, barres du diagramme, etc.).



