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
