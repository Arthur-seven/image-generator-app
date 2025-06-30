# Générateur d'images

Cette application web simple vous permet de générer des images basées sur des noms de personnages et un style artistique optionnel, en utilisant l'API de génération d'images de Gemini.

## Aperçu de l'application

Voici un aperçu de l'interface utilisateur de l'application :

![Image de l'application Générateur d'images](https://placehold.co/600x400/cccccc/333333?text=Capture+d%27écran+de+l%27application)

**Note :** Pour obtenir une capture d'écran réelle de votre application déployée, vous pouvez la lancer, prendre une capture d'écran, la télécharger sur un service d'hébergement d'images (comme Imgur, GitHub Gist, etc.) et remplacer l'URL de l'image ci-dessus par l'URL de votre capture d'écran.

## Fonctionnalités

* Génère des images pour "GENMA", "LORD GENMA", "SASAKI GENMA" et "SASAKI MD".
* Permet de spécifier un style artistique personnalisé (par exemple, "Art name", "pixel art", "cyberpunk").
* Affiche un indicateur de chargement pendant la génération de l'image.
* Affiche les messages d'erreur ou de succès.

## Comment créer le dépôt GitHub et le déployer sur Render

Suivez ces étapes pour mettre votre application sur GitHub et la déployer.

### Prérequis

* [Git](https://git-scm.com/downloads) installé sur votre ordinateur.
* Un compte [GitHub](https://github.com/).
* Un compte [Render](https://render.com/) (vous pouvez vous inscrire gratuitement).

### Étapes pour GitHub

1.  **Initialisez un dépôt Git local :**
    * Ouvrez votre terminal ou invite de commande.
    * Naviguez jusqu'à votre dossier `image-generator-app` en utilisant la commande `cd` :
        ```bash
        cd chemin/vers/votre/dossier/image-generator-app
        ```
        (Remplacez `chemin/vers/votre/dossier` par le chemin réel de votre dossier.)
    * Initialisez le dépôt Git :
        ```bash
        git init
        ```

2.  **Ajoutez les fichiers et faites votre premier commit :**
    * Ajoutez tous les fichiers de votre dossier au "staging area" :
        ```bash
        git add .
        ```
    * Validez vos modifications (créez le premier "commit") :
        ```bash
        git commit -m "Initial commit: Add image generator app"
        ```

3.  **Créez un nouveau dépôt sur GitHub.com :**
    * Accédez à [GitHub](https://github.com/) et connectez-vous.
    * Cliquez sur le bouton vert "New" (Nouveau) en haut à gauche de votre tableau de bord.
    * Donnez un nom à votre dépôt (par exemple, `image-generator-app`).
    * Choisissez si vous voulez qu'il soit `Public` ou `Private`.
    * **Très important : Ne cochez PAS** les options pour "Add a README file", "Add .gitignore", ou "Choose a license", car vous avez déjà créé vos fichiers localement.
    * Cliquez sur "Create repository" (Créer le dépôt).

4.  **Connectez votre dépôt local à votre dépôt GitHub :**
    * Après avoir créé le dépôt sur GitHub, vous verrez des instructions. Cherchez la section "…or push an existing repository from the command line".
    * Copiez les deux lignes de commande fournies. Elles devraient ressembler à ceci (remplacez `VOTRE_NOM_UTILISATEUR` et `VOTRE_REPO` par vos vraies informations) :
        ```bash
        git remote add origin [https://github.com/VOTRE_NOM_UTILISATEUR/VOTRE_REPO.git](https://github.com/VOTRE_NOM_UTILISATEUR/VOTRE_REPO.git)
        git branch -M main
        git push -u origin main
        ```
    * Collez ces commandes dans votre terminal (assurez-vous d'être toujours dans votre dossier `image-generator-app`) et appuyez sur Entrée après chaque ligne.

Félicitations ! Votre code est maintenant sur GitHub. Vous pouvez visiter `https://github.com/VOTRE_NOM_UTILISATEUR/VOTRE_REPO` pour le voir.

### "Télécharger" le dépôt (Cloner)

Une fois que votre dépôt est sur GitHub, si vous ou quelqu'un d'autre souhaitez obtenir une copie du code sur un autre ordinateur (ou même sur le même ordinateur mais dans un autre emplacement), vous pouvez utiliser la commande `git clone` :

1.  Sur la page de votre dépôt GitHub, cliquez sur le bouton vert "Code".
2.  Copiez l'URL HTTPS (par exemple, `https://github.com/VOTRE_NOM_UTILISATEUR/VOTRE_REPO.git`).
3.  Ouvrez votre terminal et naviguez jusqu'à l'emplacement où vous souhaitez enregistrer le dossier du projet.
4.  Exécutez la commande :
    ```bash
    git clone [https://github.com/VOTRE_NOM_UTILISATEUR/VOTRE_REPO.git](https://github.com/VOTRE_NOM_UTILISATEUR/VOTRE_REPO.git)
    ```
    Ceci créera une copie locale du dépôt.

### Déploiement sur Render

Une fois que votre dépôt est sur GitHub, le déploiement sur Render est simple :

1.  Accédez à [Render](https://render.com/) et connectez-vous.
2.  Dans votre tableau de bord Render, cliquez sur "New" (Nouveau) dans la barre latérale, puis sélectionnez "Static Site" (Site statique).
3.  Connectez votre compte GitHub si ce n'est pas déjà fait.
4.  Sélectionnez le dépôt GitHub que vous venez de créer (par exemple, `image-generator-app`).
5.  Configurez les paramètres de votre site statique :
    * **Name (Nom) :** Un nom unique pour votre service.
    * **Root Directory (Répertoire racine) :** Laissez vide (si `index.html` est à la racine de votre dépôt).
    * **Build Command (Commande de construction) :** Laissez vide (c'est une application HTML/JS statique).
    * **Publish Directory (Répertoire de publication) :** Laissez vide.
6.  Cliquez sur "Create Static Site" (Créer un site statique).

Render détectera automatiquement les modifications dans votre dépôt GitHub et déploiera votre application. Une fois le déploiement terminé, Render vous fournira une URL publique pour accéder à votre générateur d'images !
