# Bienvenue sur ce repo consacré à l'apprentissage du framework Rails

#### Les concepts qui vont être expliqués ici sont :

* La différence entre un site statique et un site dynamique.
* Le MVC.
* Les routes.
* Les Bases de Données.
* GET / POST.
* Le concept de migration.
* Les relations entre les models des BDD.
* Les fonctions du CRUD.

## 1. La différence entre un site statique et un site dynamique
Un **_site statique_** est un site qui ne bouge pas, comme son nom l'indique ! Plus concrètement, c'est une site qui affichera toujours la même page peu importe qui l'utilise. Ce sont des sites bien souvent **peu avancés**. 
<br />
![schéma site statique](https://image.noelshack.com/fichiers/2018/05/1/1517240782-statique.jpg)
<br />

En effet, les sites les plus utilisés de nos jours proposent tous un système de log in, cela les force à être **_dynamiques !_**

Effectivement, les **_sites dynamiques_** sont les sites capables d'afficher un contenu particulier en fonction de la personne navigant sur ce site. Cette navigation dynamique requiert un accès permanent à la **base de données** du site.
La personne navigant sur le site n'est pas le seul paramètre qui peut influencer l'affichage du site ! Des paramètres comme l'heure, la date, l'adresse IP de la machine s'y connectant sont aussi le lot des sites dynamiques !
<br />
![schéma site dynamique](https://image.noelshack.com/fichiers/2018/05/1/1517240786-dynamique.png)
<br />
<br />
En conclusion, la différence majeure entre un site statique et un site dynamique est le fait que le **premier affiche toujours le même contenue** et le **second varie en fonction de la demande**.

## 2. Le MCV (Model View Controller)
Le Modèle-Vue-Controleur en français est un **motif** créé dans le but de mettre en place des interfaces utilisateur, donc, vous l'aurez compris, de créer un _site dynamique_ !
Il est composé comme son nom l'indique de 3 entités principales:

<br />

![Schéma du MVC](https://image.noelshack.com/fichiers/2018/05/1/1517241703-mvc.png)

<br />

* Un modèle qui est chargé d'échanger avec la database pour pouvoir fournir au contrôleur les données à afficher.
* Une vue qui contient la présentation de l'interface graphique.
* Un contrôleur qui contient l'ensemble des actions logiques que l'utilisateur souhaite mettre en oeuvre sur son site.

## 3. Les routes
Les routes permettent de faire le lien entre la "demande" du navigateur (donc l'_URL_) et le contrôleur.
Elles permettent donc de définir quel contrôleur va être utilisé en fonction de l'URL.

<br />

![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `#f03c15`

Dans un framework rails, on les trouve dans config/routes.rb
On y utilise principalement des "get" qui prennent une URL et qui envoient vers un contrôleur
