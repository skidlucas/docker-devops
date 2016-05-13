## Tutoriel d'utilisation TP Docker

Dans un premier temps:

1. `git clone https://github.com/skidlucas/docker-devops.git`
2. `cd docker-devops`


### Avec deux images en local

On supposera que skidlucas est votre pseudonyme.

1. `cd backend && docker build -t skidlucas/backend .`
2. `cd ../banking && docker build -t skidlucas/banking .` 

Dans deux terminaux différents:

`docker run -p 9090:9090 skidlucas/banking` <br />
`docker run -p 8080:8080 skidlucas/backend`

Puis on lance le client comme d'habitude, depuis notre IDE préféré ou avec `mvn exec:java` dans le dossier client.
<br />
<br />

### Pour lancer les images sur plusieurs machines

Il faudrait changer à la main l'adresse IP dans TCF, plus précisément dans *j2e/src/main/resources/bank.properties* et dans *j2e/src/main/java/.../utils/BankAPI.java*, en remplaçant localhost par l'adresse IP de la machine qui lance le serveur .NET. Ensuite, il faudrait build de nouveau le war **tcf-backend.war** et remplacer le war présent dans le dossier *docker-devops/backend*.
<br />
<br />


### Avec Docker compose

En supposant que vous êtes dans le dossier *docker-devops* et que vous avez déjà build les deux images précédemment, remplacez *skidlucas* par votre pseudo dans le fichier **docker-compose.yml** et puis il suffit de faire `docker-compose up` pour lancer les deux serveurs. Ensuite, on lance le client comme précédemment.
<br />
<br />

Lucas Martinez <br />
Simon Paris <br />
Lucas Soumille <br />

