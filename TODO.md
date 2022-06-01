
## Modifications pour le POC

### 3 pb dans le code :

- Il scanne tous les environnement, 
il faudrait mettre un filtre pour ne récupérer que les données de « prod » par exemple ce qui saturera moins les API
 de Sentry. 

- Il ne récupère que le détail des infos des sujets de moins d’une heure, 
je pense que l’on devrait faire la même chose pour les status à 24h et 14d. 

- Il ne récupère que l’id. je propose d’ajouter aussi les champs shortId et title 
(ex : "shortId":"SERVICE-SPORT-CLIENTPRO-FUNCTIONS-10EQ", "title":"Error: Internal error encountered.") 
pour que l’on puisse mieux identifier la nature des erreurs par la suite.

### TODO

- Faire les modifications du code
    - ajout de la variable d’environement SENTRY_EXPORTER_ENVS qui liste les environements à prendre en compte. 

- Faire une version Docker 

- Brancher l’instance Docker Prometheus dessus

- Brancher une instance Grafana dessus (prendre les exemples conseillés dans la documentation)

