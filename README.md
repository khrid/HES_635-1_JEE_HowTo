# HES_635-1_JEE_HowTo

> :warning: **Work in progress**

Ce repository a pour but d'expliquer la mise en place de l'environnement de développement pour le cours **635-1 JEE** de la HES-SO Valais/Wallis avec [IntelliJ Ultimate](https://www.jetbrains.com/fr-fr/community/education/#students).

## Infos
Cette marche à suivre suppose l'organisation suivante :
 - **Un** projet contiendra l'ensemble du cours
 - Les différents TP / exercices seront gérés dans des **modules**

# Configuration d'IntelliJ
## Installation de la version de Java
Suivre les étapes sur Cyberlearn pour télécharger et installer l'OpenJDK 14.0.2.

## Préparation du projet
Dans IntelliJ, créer un nouveau projet via le menu `File > New > Project`. Dans la fenêtre `New Project`, sélectionner `Empty Project`.

Cliquer sur `Next` puis saisir le nom du projet souhaité.
![image](https://user-images.githubusercontent.com/389415/110202011-67e8b500-7e66-11eb-8b01-5d4c521deaac.png)

Ouvrir le projet nouvellement créé.

Dans la fenêtre `Project Structure` qui va s'afficher, cliquer sur Project dans le menu de gauche. et s'assurer que le SDK utilisé est celui configuré précédemment.

![image](https://user-images.githubusercontent.com/389415/110218505-6e088100-7eba-11eb-8daf-31622addb4ed.png)


## Création de la structure
Ouvrir le projet dans l'explorateur de fichier, et créer les dossiers suivants :

![image](https://user-images.githubusercontent.com/389415/110202203-6966ad00-7e67-11eb-8646-2eb97c454ce5.png)

### database
Copier le contenu du dossier `database` fourni sur Cyberlearn dans le dossier database créé.

![image](https://user-images.githubusercontent.com/389415/110202219-78e5f600-7e67-11eb-817b-f9953f7c41dc.png)

### tools
Copier le contenu du dossier `tools` fourni sur Cyberlearn dans le dossier database créé.

![image](https://user-images.githubusercontent.com/389415/110202232-8c915c80-7e67-11eb-90d9-a35313ddf3f3.png)

## Import de la structure dans Intellij
Dans Intellij, clic sur le menu `File > Project Structure`. Aller dans `Modules`, puis cliquer sur le `+`. `New Module`. Sélectionner `Java` dans la liste déroulante, puis `Next`. Dans `Content root`, **sélectionner la racine du projet**:

![image](https://user-images.githubusercontent.com/389415/110218752-ac527000-7ebb-11eb-9913-0769b1d0fdcc.png)

Clic sur `Finish`, puis `Apply`.

![image](https://user-images.githubusercontent.com/389415/110218792-e459b300-7ebb-11eb-952b-4af822ad6cbe.png)

## Configuration du serveur d'application
Ouvrir les paramètres via le menu `File > Settings`, puis aller dans le menu `Build, Execution, Deployment | Application Servers`. Cliquer sur le `+` pour ajouter un nouveau `JBoss server`.

![image](https://user-images.githubusercontent.com/389415/110219437-84fda200-7ebf-11eb-9dd3-74a046a58913.png)

Rechercher l'emplacement du serveur Wildfly qui se trouve dans le dossier `tools`.

![image](https://user-images.githubusercontent.com/389415/110219461-b4141380-7ebf-11eb-9126-76db0aa420ff.png)

Valider en cliquant sur `OK`.

![image](https://user-images.githubusercontent.com/389415/110219479-c2fac600-7ebf-11eb-955d-9b654d8df66f.png)

Les libraries se chargent, puis le serveur est ajouté. Il est possible de le renommer si souhaité.

# Mise en place des TP
## Projet maven (TP1)
Le TP1 est particulier car il n'utilise pas la technologie Java Entreprise. Il sert de démonstration aux limitations existantes.

### Configuration

Dans IntelliJ, créer un nouveau module via le menu `File > New > Module`. Dans la fenêtre `New Module`, sélectionner `Maven`.
Cliquer sur `Next`. Renseigner les champs suivants selon la capture, puis cliquer sur `Finish`

![image](https://user-images.githubusercontent.com/389415/110218476-42859680-7eba-11eb-9deb-8267fcbd151a.png)

Le module est créé.

![image](https://user-images.githubusercontent.com/389415/110218804-ede31b00-7ebb-11eb-9309-3ddbeb650f8e.png)

Télécharger le zip avec la donnée du TP depuis Cyberlearn, puis l'ouvrir via l'explorateur de fichier. Copier le contenu du dossier `src` dans le dossier `src` du TP1 dans IntelliJ. Les fichiers `.class` peuvent être ignorés.

Dans IntelliJ, ouvrir le fichier pom.xml et remplacer le contenu par celui du [pom.xml adapté](src/tp1/pom.xml).

Cliquer sur l'icône ![image](https://user-images.githubusercontent.com/389415/110219114-87f79300-7ebd-11eb-90b7-b8c6ffe6b98f.png) qui s'affiche pour charger les changements effectués dans le pom.xml.

![image](https://user-images.githubusercontent.com/389415/110219123-ab224280-7ebd-11eb-8685-42243f701c9b.png)

Cliquer sur ![image](https://user-images.githubusercontent.com/389415/110218932-a6a95a00-7ebc-11eb-832b-82d9b71d5394.png) pour builder le projet.

![image](https://user-images.githubusercontent.com/389415/110219138-c3925d00-7ebd-11eb-9039-8d542ff18e21.png)

### Test
:warning: **Ne pas oublier de démarrer la base de données et de la populer.**
 
Ouvrir le fichier `src/main/java/ch/hevs/test/TestClient`, et exécuter le code de la classe.

![image](https://user-images.githubusercontent.com/389415/110219203-1ec44f80-7ebe-11eb-8a6d-531e68270838.png)

```
1-Zidane-Zinedine
2-Platini-Michel
3-Papin-Jean-Pierre
Client inserts in the database the id 4
Client 4 modified

Process finished with exit code 0
```
Le code s'exécute avec succès.

## Projet Java Entreprise (TP2 et suivants)
### Configuration

Dans IntelliJ, créer un nouveau module via le menu `File > New > Module`. Dans la fenêtre `New Module`, sélectionner `Java Entreprise`. S'assurer que le paramètre `Application server` corresponde à celui configuré précédemment. 

![image](https://user-images.githubusercontent.com/389415/110219576-6c41bc00-7ec0-11eb-86c4-e7e0b1b19acf.png)

Cliquer sur `Next`. Suivant le TP, ajouter les librairies nécessaires (par exemple `Servlet`, `Server Faces`, etc..). Cliquer sur `Next`, puis renseigner l'emplacement du module selon la capture, puis `Finish`.

![image](https://user-images.githubusercontent.com/389415/110219649-d78b8e00-7ec0-11eb-9399-cf87ea086f21.png)

Le module est créé.

![image](https://user-images.githubusercontent.com/389415/110218804-ede31b00-7ebb-11eb-9309-3ddbeb650f8e.png)

Une nouvelle configuration de déploiement a été créée automatiquement :

![image](https://user-images.githubusercontent.com/389415/110219668-fbe76a80-7ec0-11eb-8a54-e39f1a304881.png)

![image](https://user-images.githubusercontent.com/389415/110219672-00138800-7ec1-11eb-8879-13d2959df520.png)


Télécharger le zip avec la donnée du TP depuis Cyberlearn, puis l'ouvrir via l'explorateur de fichier. Copier le contenu du dossier `src` dans le dossier `src` du TP1 dans IntelliJ. Les fichiers `.class` peuvent être ignorés.

Dans IntelliJ, ouvrir le fichier pom.xml et remplacer le contenu par celui du [pom.xml adapté](src/tp2+/pom.xml).

Cliquer sur l'icône ![image](https://user-images.githubusercontent.com/389415/110219114-87f79300-7ebd-11eb-90b7-b8c6ffe6b98f.png) qui s'affiche pour charger les changements effectués dans le pom.xml.

![image](https://user-images.githubusercontent.com/389415/110219123-ab224280-7ebd-11eb-8685-42243f701c9b.png)

Cliquer sur ![image](https://user-images.githubusercontent.com/389415/110218932-a6a95a00-7ebc-11eb-832b-82d9b71d5394.png) pour builder le projet.

![image](https://user-images.githubusercontent.com/389415/110219138-c3925d00-7ebd-11eb-9039-8d542ff18e21.png)

### Test
:warning: **Ne pas oublier de démarrer la base de données et de la populer.**

Exécuter la configuration créée par défaut en cliquant sur le bouton vert ![image](https://user-images.githubusercontent.com/389415/110219922-6947cb00-7ec2-11eb-92a5-8345f7e6ef80.png)

Le serveur Wildfly va démarrer, puis un nouvel onglet va s'ouvrir.

![image](https://user-images.githubusercontent.com/389415/110219999-00ad1e00-7ec3-11eb-9300-d0af71ff5372.png)

Il est possible d'avoir le message `404 - Not found`. Dans ce cas, s'assurer de l'URL de déploiement dans les logs : 
`21:25:43,248 INFO  [org.jboss.as.server.deployment] (MSC service thread 1-3) WFLYSRV0027: Starting deployment of "TP02-WEB-JSP-SERVLET-E-0.0.1-SNAPSHOT" (runtime-name: "TP02-WEB-JSP-SERVLET-E-0.0.1-SNAPSHOT.war")`

ainsi que du nom du fichier (x)html dans le dossier `webapp`
