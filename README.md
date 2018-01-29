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
![Schéma du MVC](https://image.noelshack.com/fichiers/2018/05/1/1517235673-68747470733a2f2f7777772e737570696e666f2e636f6d2f61727469636c65732f7265736f75726365732f3137353236382f3737372f312e706e67.png)
<br />

