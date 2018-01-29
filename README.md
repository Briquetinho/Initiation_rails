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

Dans un framework rails, on les trouve dans config/routes.rb
On y utilise principalement des "get" qui prennent une URL et qui envoient vers un contrôleur comme dans l'exemple ci dessous : 
```ruby
get '/welcome', to: "pages#welcome"
```
<br />
Ici, pour une URL se terminant par welcome, on se redirigera vers le contrôleur "pages".

<br />
<br />

On peut aussi utiliser "root" à la place de "get" pour parler de la page d'accueil du site :
```ruby
root :to =&gt; 'pages#main'
```
<br />

## 4. Les Bases de Données

Une base de données est un ensemble structuré et organisé de données. On peut par exemple se représenter ça comme un ensemble de fichiers spreadsheet qui sont liés entre eux selon certaines données comme leur ID ou leurs titres.
Rails permet de créer plusieurs fichiers qui peuvent nous montrer l'état des lieux des bases de données grâce à la commande `rails db:migrate`

<br />

## 5. GET / POST

GET et POST sont deux types de requêtes différentes:

- **GET** : Les données sont ajoutées à l'URI(URL ou URN), les données sont transmises de l'ordinateur au serveur. Elles sont *visibles* par tous ! Ce type de paramêtre est appelé **chaine de requête**.

- **POST** : Les données sont incluses dans le formulaire HTML. Elles sont déjà présente sur le serveur et sont *invisibles*. Cette méthode est utilisée la plupart du temps pour créer une nouvelle ressource.

<br />

## 6. La migration

Les migrations permettent de faire évoluer le schéma de nos bases de données au cours du temps. C'est une forme de **simplification du language** pour la modification des bases de données.
Plutôt que d'écrire des commandes de modification de la base de données en pur SQL, la migration nous permet de décrire facilement les changements qu'on désire y faire.

Pour plus d'informations sur la migration, vous pouvez vous renseigner sur ce [guide](http://edgeguides.rubyonrails.org/active_record_migrations.html)

<br />

## 7. Les relations entre les modèles et les bases de données

Un modèle de bases de données définit entre autres **la structure logique** de cette base de données. Il existe beaucoup de modèles de bases de données différentes, mais comme pour les langages de programmation, certains sont plus utilisés que d'autres. Voici une liste des modèles les plus utilisés:

- Modèle de base de données hiérarchique
- Modèle relationnel
- Modèle réseau
- Modèle de base de données orientée objet
- Modèle entité-association
- Modèle document
- Modèle entité-attribut-valeur
- Schéma en étoile
- Le modèle relationnel-objet, qui associe les deux éléments qui composent son nom

Ce [**site**](https://www.lucidchart.com/pages/fr/quest-ce-quun-mod%C3%A8le-de-base-de-donn%C3%A9es) explique très bien chacun de ces modèles !

<br />

## 8. Les fonctions du CRUD

CRUD signifie "Create-Read-Update-Destroy". Il s'agit des 4 actions qui servent à manipuler les **bases de données relationelles**.
Ces termes sont assez clairs sur ce qu'ils font. Il peut cependant être intéressant de relier ces opérations à des méthodes HTTP.
En effet, on retrouve le GET et le POST du **5.**, qui sont des méthodes HTTP, et qui correspondent respectivement aux opérations READ et CREATE.
Pour les opérations  Update et Destroy, les méthodes HTTP correspondantes sont PUT et DELETE.

<br />
____

Merci d'avoir lu ce readme, j'espère que certains termes sont maintenant plus clairs pour vous :bowtie:





