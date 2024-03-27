# Créer un fichier package.json

=> npm init -y

Le fichier package.json permet de :

. Lister les paquets utilisés par votre projet qui sont appelés ses dépendances. En effet, sans ces paquets, votre projet ne fonctionne pas, il est donc bien dépendant de celles-ci.

. Spécifier précisément quelles versions des dépendances peuvent être installées.

. Permettre aux développeurs d'installer toutes les dépendances de votre projet en une commande.

# Installation de dépendance : sass

=> npm i sass

Ces paquets seront installés dans le dossier node_modules et seront ajoutés comme
dépendance dans le fichier package.json :

{
"name": "my_package",
"version": "1.0.0",
"dependencies": {
"ma_dependance": "^1.0.0",
}
}

# créer notre script

{
"name": "sass",
"version": "1.0.0",
"description": "",
"main": "index.js",
"scripts": {
"sass": "sass -w scss:css"
},
"keywords": [],
"author": "",
"license": "ISC",
"dependencies": {
"sass": "^1.32.11"
}
}

Dans notre fichier package.json, vous remarquez qu'il y a une entrée scripts.

Ces scripts peuvent être lancés en faisant npm run nom-du-script.

. sass permet de lancer la librairie sass.

. --watch ou -w : permet d'indiquer le dossier ou les fichiers contenant les fichiers Sass qui vont être suivis et converti en CSS automatiquement.

. --output ou -o : permet d'indiquer le dossier où seront mis les fichiers CSS convertis depuis le Sass.

# lancer le script

=> npm run sass.

# Le fichier .gitignore

Lorsque vous utilisez des dépendances, vous avez un dossier node_modules qui contient toutes les dépendances installées.

Or, ces dépendances prennent beaucoup de place en général et nous ne souhaitons pas sauvegarder les changements des versions de ces dépendances lors des mises à jour etc.

En outre, il est très facile grâce aux fichiers package.json et package-lock.json d'installer toutes les dépendances de votre projet avec exactement la version que vous aviez.

Votre équipe ou vous-même sur une autre machine pouvez donc très simplement réinstaller toutes les dépendances en faisant npm install.

Pour ces raisons, nous voulons dire à Git de ne pas suivre les changements et donc de ne pas ajouter à notre dépôt tout le contenu de ce dossier.

Pour ce faire, il suffit de créer un fichier spécial, ayant forcément pour nom .gitignore dans le dossier de votre projet.

Dans ce fichier, il suffit de mettre :

=> node_modules
