```

                                    _  _    ___     ___     __  __                 _ ____  _____ 
  _ __ ___   ___  _ __   __ _  ___ | || |  / _ \   ( _ )   |  \/  |_   _ ___  __ _| | ___||___  |
 | '_ ` _ \ / _ \| '_ \ / _` |/ _ \| || |_| | | |  / _ \/\ | |\/| | | | / __|/ _` | |___ \   / / 
 | | | | | | (_) | | | | (_| | (_) |__   _| |_| | | (_>  < | |  | | |_| \__ \ (_| | |___) | / /  
 |_| |_| |_|\___/|_| |_|\__, |\___/   |_|(_)___/   \___/\/ |_|  |_|\__, |___/\__, |_|____(_)_/   
                        |___/                                      |___/        |_|              
           
```

### Stack ###

L'environnement de dev se repose sur [DOCKER](https://docker.com) / 
[MYSQL](https://hub.docker.com/_/mysql) / 
[PHPMYADMIN](https://hub.docker.com/r/phpmyadmin/phpmyadmin/) / 
[MONGO](https://hub.docker.com/_/mongo) /
[MONGO-EXPRESS](https://hub.docker.com/_/mongo-express)

@autor : Benoit Foujols \
@version : 3.1.0 

### Acces au service

| Version | Service           | URL                                                    |
|:--------|:------------------|:-------------------------------------------------------|
| 5.7     | Mysql             | mysql://127.0.0.1:3306                                 |
| 4.0     | Mongo             | mongo://127.0.0.1:2717                                 |
| -       | PhpMysqlAdmin         | [http://localhost:8082/](http://localhost:8082/)       |
| -       | Mongo Express | [http://localhost:8081/](http://localhost:8081/) |

Login : root \
Password : yoo
/!\ Celui-ci peut être changer dans le fichier docker-compose
---
### Installation "docker-compose" ###

Fonctionnement 

1. Téléchargement du projet
```
$ git clone git@github.com:bfoujols/docker-db-mysql-mongodb.git
```
2. Modifier le fichier docker-composer.yml
```
$ cp exempl_docker-composer.yml docker-composer.yml
$ vim docker-composer.yml
<<<
11      MYSQL_ROOT_PASSWORD: ****
12      MYSQL_DATABASE: app_db
13      MYSQL_USER: ****
14      MYSQL_PASSWORD: ****
>>>
```
3. Creation de l'environnement docker
```
$ sudo docker-compose create
```
4. Demarrer l'environnement docker
```
$ sudo docker-compose start
```
5. Stop l'environnement docker
```
$ sudo docker-compose stop
```
6. Rebuild l'environnement docker
```
$ sudo docker-compose rm
```

---

#### Autres commandes ####

Voir les processus
```
$ sudo docker ps -a
```

Killer un processus 
```
$ sudo docker kill -f f9fa1f1c0d29
```

Voir les images 
```
$ sudo docker ps -a
```

Supprimer un conteneur 
```
$ sudo docker rm -f 1a7a672f0fbd
```

Supprimer une image 
```
$ sudo docker rmi -f 1a7a672f0fbd
```

Entrée en shell : 
```
$ docker exec -it 04d713497315 /bin/bash
```
---