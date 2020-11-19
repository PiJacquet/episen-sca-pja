Commande de builds:
- Front: docker build -t pjacquet/episen-sca-pja-front .
- Back : docker build -t pjacquet/episen-sca-pja-back .

Sachant que nginx n'est pas lancé en root, le port à été changé vers 8081
URL du front http://localhost:8081

Docker-compose :
docker-compose up

NB sur docker-compose:
Les tests sont réalisés par des curl (installés lors du dockerfile). Pour le post, une valeur POST est envoyé toutes les 30s.
Vu que le mécanisme de LB n'était pas demandé, 2 replicas sont demandés avec un maximum d'un par node (problème d'appropriation du port au dessus)

URL des repo :
- Front: https://hub.docker.com/repository/docker/pjacquet/episen-sca-pja-front
- Back : https://hub.docker.com/repository/docker/pjacquet/episen-sca-pja-back