Commande de builds:
-Front: docker build -t pjacquet/episen-sca-pja-front .
-Back : docker build -t pjacquet/episen-sca-pja-back .

Sachant que nginx n'est pas lancé en root, le port à été changé vers 8081
URL du front http://localhost:8081

Docker-compose :
docker-compose up

NB sur docker-compose:
Les tests sont réalisés par des curl (installés lors du dockerfile). Pour le post, une valeur POST est envoyé toutes les 30s.
Vu que le mécanisme de LB n'était pas demandé, les replicas ont été laissés dans la config à 1 (problème d'appropriation du port au dessus)