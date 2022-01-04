# Quizz

## But

- construire une application de quizz en Vue.js
- consommer une API
- écrire des tests pertinents

## Explications

Le but de cet exercice est de créer une application Web de quizz, en Vue.js.
Elle se composera d'un écran affichant le quizz (questions + réponses), la validation se fera côté frontend.
À la fin du quizz, le score est affiché à l'utilisateur (disons 1 point par bonne réponse), et il lui sera demandé un nom d'utilisateur. Après avoir soumis ce formulaire, un message de confirmation de la sauvegarde apparaît.

Le design est libre et l'installation des plugins Vue est, bien entendu, autorisée.

Cette application consommera une API composée de deux endpoints :

- Un GET pour récupérer toutes les questions avec les réponses associées.
- Un POST pour sauvegarder le résultat de l'utilisateur.

La spec complète est présente ici : [api.yaml](doc/api.yaml).

Le backend est simulé via cette spécification.

L'application a été installée dans le répertoire [app](app/) et ne contient actuellement qu'un bootstrap Vue.js. Elle sera donc à compléter.

## Prérequis

Docker et Docker Compose sont nécessaires.

## Installation

- Merci de créer un fork.
- Une fois sur votre machine, démarrer les services Docker :
  ```bash
  cd vuejs-ex/quizz
  docker-compose up --build
  ```
- Pour accéder à la console de l'application :
  ```bash
  docker-compose exec app sh
  ```
- Après avoir lancé le serveur Vue, l'application sera accessible via le port 8080 : http://localhost:8080
- Le backend est accessible par le port 4010 : http://localhost:4010
- Les logs du service de mock sont visibles dans l'output du docker-compose up, ou en tapant :
  ```bash
  docker-compose logs -f mock
  ```
