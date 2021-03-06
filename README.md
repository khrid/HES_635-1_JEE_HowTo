# HES_635-1_JEE_HowTo

> :warning: **Work in progress**

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
Dans Intellij, créer un nouveau module via le menu `File > Project Structure`. Aller dans `Modules`, puis cliquer sur le `+`. `New Module`. Sélectionner `Java` dans la liste déroulante, puis `Next`. Dans `Content root`, **sélectionner la racine du projet**:

![image](https://user-images.githubusercontent.com/389415/110218752-ac527000-7ebb-11eb-9913-0769b1d0fdcc.png)

Clic sur `Finish`, puis `Apply`.

![image](https://user-images.githubusercontent.com/389415/110218792-e459b300-7ebb-11eb-952b-4af822ad6cbe.png)


## Projet maven (TP1)
Le TP1 est particulier car il n'utilise pas la technologie Java Entreprise. Il sert de démonstration aux limitations existantes.

Dans Intellij, créer un nouveau module via le menu `File > New > Module`. Dans la fenêtre `New Module`, sélectionner `Maven`.
Cliquer sur `Next`. Renseigner les champs suivants selon la capture, puis cliquer sur `Finish`

![image](https://user-images.githubusercontent.com/389415/110218476-42859680-7eba-11eb-9deb-8267fcbd151a.png)

Le module est créé.

![image](https://user-images.githubusercontent.com/389415/110218804-ede31b00-7ebb-11eb-9309-3ddbeb650f8e.png)


## Projet Java Entreprise (TP2 et suivants)
