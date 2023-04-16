
# Wiki-App
## Table des matières
 - [Fonctionalitées](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#fonctinalit%C3%A9es)
 - [Descriptif de l'application](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#descriptif)
 - [Diagramme](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#diagramme)
 - [Les méthodes](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#m%C3%A9thodes)
  - [La pagination](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#pagination)
 -  [Vue d'ensemble de l'application](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#m%C3%A9thodes)
  - [Déploiement](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#d%C3%A9ploiment)
   - [L'api](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#lien-api)

 - [Conclusion](https://github.com/RodyGuemegah/wikiE6/edit/main/README.md#conclusion)
## Fonctinalitées

- Visual Studio code
- Boosstrap 5
- Angular
- HTML


## Descriptif

Le projet Wiki-App consiste à développer une application
Front-end en utilisant le framework Angular, pour des recherches diverses et ainsi afficher les
pages wikipédia associés.
Nous utiliserons une API présente sur un serveur distant..
L'application utilisent plusieurs component dont les principaux sont le app.component.ts
(affiche une barre de recherche, ),
wiki.service.ts qui récupère pour effectuer des requêtes HTTP à l'API de recherche de Wikipedia.

## Diagramme
- Voici mon diagramme
avec le client qui effectue une recherche sur l'application 
ce qui envoie une requête vers l'api qui donne les informations requises pour afficher le contenu de la page associée.
![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/diagramme.png?raw=true)



###  Méthodes 
#### app.component.html
- La méthode principale pour ce composant est une méthode onSubmit() qui est déclenchée
lorsqu'un formulaire est soumis. Cette méthode utilise un service wiki pour effectuer une recherche
à l'aide d'un terme de recherche spécifié par l'utilisateur (this.searchTerm).
- La méthode search() retourne un observable qui émet une réponse HTTP de l'API Wikipedias.
- La méthode subscribe() est utilisée pour s'abonner à l'observable et traiter la réponse. La réponse est de type any.
Puis, la méthode console.log() est utilisée pour afficher les résultats de la recherche dans la
console pour le débogage et la vérification.

![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/Capture%20d%E2%80%99%C3%A9cran%202023-04-06%20145557.png?raw=true)



#### app.component.html

Ce code représente un formulaire de recherche simple dans un fichier HTML. La méthode
onSubmit() est appelée lorsque le formulaire est soumis en utilisant l'événement (submit).
Le formulaire contient un champ de saisie de texte qui utilise la directive ngModel pour lier la
valeur de searchTerm à l'entrée de l'utilisateur. La valeur de searchTerm sera mise à jour à chaque
fois que l'utilisateur saisira quelque chose dans le champ de saisie
Le formulaire contient également un bouton de soumission avec une classe btn btn-lg btn-primary.
Lorsque l'utilisateur clique sur le bouton, la méthode onSubmit() est appelée et le formulaire est
soumis.
![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/html.png?raw=true)

#### Pagination
Ce code présente une boucle *ngFor et affiche les résultats de la recherche sur la page. Il y a
également une directive “paginate” qui permet de diviser les résultats en pages, en affichant 10
résultats par page.
Les variables page et totalResults sont utilisées pour la pagination et pour calculer le nombre total
de résultats.
Pour chaque résultat de recherche, il y a un lien qui redirige vers la page Wikipedia
correspondante, en utilisant le pageid de chaque résultat. Le titre de la page est affiché.


![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/pagination,html.png?raw=true)

#### Vue application
- voici une capture d'écran d'une recherche effectuer sur l'application avec la barre de recherche et les recherches associées.
![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/recherche.png?raw=true)

#### Routes 
![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/routes.png?raw=true)







## Déploiment
#### voici  la commande permettant le déploiement de notre application
```bash
npm install firebase
```
- Notre application a été déployer sur firebase qui est une interface graphique permettant l'hosting d'application.
- ci-dessous l'extrait de ce code montre les paramètres de configuration pour l'hebergement de notre application.
![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/deploiement.png?raw=true)





## Lien API

Voici le lien de notre API qui est une API distante

`https://en.wikipedia.org/w/api.php`

#### wiki.service.ts
- La méthode search du service envoie une requête GET à l'API de recherche de Wikipedia en
utilisant l'URL de base baseURL.
Ensuite différent paramètre sont inclue:
- ‘action’ : spécifie l'action que l'API doit effectuer. Dans ce cas, il s'agit de la recherche de
pages.
-  ‘format’ : spécifie le format de la réponse. Dans ce cas, il s'agit d'un objet JSON.
- ‘list’ : spécifie la liste des résultats que l'on souhaite obtenir. Dans ce cas, il s'agit de la liste
de résultats de recherche.
- ‘srsearch’ : spécifie le terme de recherche pour lequel on souhaite obtenir des résultats.
- ‘origin’ : spécifie l'origine de la requête pour éviter les erreurs de CORS.
- ‘srlimit’ : spécifie le nombre maximum de résultats de recherche que l'on souhaite obtenir.
![App Screenshot](https://github.com/RodyGuemegah/wikiE6/blob/main/Screenshots/wikiservice.png?raw=true)


## Conclusion

la conception de cette application ma permis d'aquerir de nouvelles compétences dans l'utilisation du framework angular. Mais aussi dans la manipulation d'une API distante.




