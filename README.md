# Créer un fichier package.json

=> npm init -y

Le fichier package.json permet de :
. Lister les paquets utilisés par votre projet qui sont appelés ses dépendances. En effet, sans ces paquets, votre projet ne fonctionne pas, il est donc bien dépendant de celles-ci.
. Spécifier précisément quelles versions des dépendances peuvent être installées.
. Permettre aux développeurs d'installer toutes les dépendances de votre projet en une commande.

# Installation de dépendance : sass

=> npm i sass

Ces paquets seront installés dans le dossier node_modules et seront ajoutés comme dépendance dans le fichier package.json :
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

Nous pouvons ensuite lancer le script en faisant npm run sass.
