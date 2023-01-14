# Docker


En entreprise on voit que de plus en plus de choses sont automatisées avec le devops, notamment les chaînes de déploiement. En tant que développeur junior on ne voit pas toujours ce qui se passe après le développement. Alors ok mon code est pushé, il a été mergé et après ? J'ai commencé à m'intéresser à la question quand j'ai voulu déployer un site web perso. Par exemple cette Github Pages est configurée pour se déployer automatiquement à chaque push du coup je n'ai pas trop à me soucier de ce qu'il se passe. 

Mais pour un vrai site web ? J'ai commencé à développer un site en Spring/Thymeleaf car c'est ma stack pro et je voulais un site pour m'entrainer et bidouiller. Je voyais tout le monde parler de Netlify et de sa facilité de déploiement, je pensais que ça me prendrait que quelques minutes. Sauf que voilà ça gère le static mais pas le java.

Du coup pour déployer mon site je dois générer une image Docker et la déployer. L'angoisse. J'ai jamais vu ça en formation.

L'objectif de cette note sera de :
* Installer Docker
* Comprendre comment ça marche un container
* Générer une image Docker

Pour aller plus loin et la déployer, on ira voir comment marche fly.io

Source : https://www.youtube.com/watch?v=3hol91BkYHU&list=PLmw3X80dPdlyRV2EUKnFOvBACs_tcArd0

## Installation sur Windows

Rendez-vous sur le site de Docker pour télécharger et installer Docker Desktop
https://docs.docker.com/desktop/install/windows-install/



## Image

Réprésentées par un id (imageID) et un nom (repository)
Le nom pointe vers un imageID
Plusieurs noms peuvent pointer vers une même image.
Chaque image contient plusieurs couches (layers)
L'image contient tout ce qui est nécessaire au lancement d'une application.

Afficher la liste des images disponibles
docker images

Filtrer la liste des images
docker images --filter reference="commencepar*:*finipar"

Lister les images non utilisées
docker images -f dangling=true

Supprimer image
docker images rmi ubuntu:latest

## Layers

Les layers font partie d'une image
Layers sont en lecture seule, ne peuvent être modifiés
Layers identifiés par un id



## Container
