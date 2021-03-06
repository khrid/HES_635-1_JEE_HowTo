# HES_635-1_JEE_HowTo
Ce repository a pour but d'expliquer la mise en place de l'environnement de développement pour le cours **635-1 JEE** de la HES-SO Valais/Wallis avec [IntelliJ Ultimate](https://www.jetbrains.com/fr-fr/community/education/#students).

## Infos
Cette marche à suivre suppose l'organisation suivante :
 - **Un** projet contiendra l'ensemble du cours
 - Les différents TP / exercices seront gérés dans des **modules**

## Installation de la version de Java

## Préparation du projet
Dans Intellij, créer un nouveau projet via le menu `File > New > Project`. Dans la fenêtre `New Project`, sélectionner `Empty Project`.

Cliquer sur `Next` puis saisir le nom du projet souhaité.
![image](https://user-images.githubusercontent.com/389415/110202011-67e8b500-7e66-11eb-8b01-5d4c521deaac.png)

Ouvrir le projet nouvellement créé

## Création de la structure
Ouvrir le projet dans l'explorateur de fichier, et créer les dossiers suivants :

![image](https://user-images.githubusercontent.com/389415/110202203-6966ad00-7e67-11eb-8646-2eb97c454ce5.png)

### database
Copier le contenu du dossier `database` fourni sur Cyberlearn dans le dossier database créé.

![image](https://user-images.githubusercontent.com/389415/110202219-78e5f600-7e67-11eb-817b-f9953f7c41dc.png)

### tools
Copier le contenu du dossier `tools` fourni sur Cyberlearn dans le dossier database créé.

![image](https://user-images.githubusercontent.com/389415/110202232-8c915c80-7e67-11eb-90d9-a35313ddf3f3.png)

## Projet maven (TP1)
Le TP1 est particulier car il n'utilise pas la technologie Java Entreprise. Il sert de démonstration aux limitations existantes.

Dans Intellij, créer un nouveau module via le menu `File > New > Module`. Dans la fenêtre `New Module`, sélectionner `Maven`.
Cliquer sur `Next`.


## Projet Java Entreprise (TP2 et suivants)
