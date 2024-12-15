---
title: Installer un « vrai » éditeur de texte
layout: page
---

Therion utilise différents types de fichiers pour :

* les données topographiques en elle-mêmes,
* les données sources des dessins
* les fichiers liaisons dans le cas de topographies complexes ou de systèmes karstiques
* les fichiers de configuration et de compilation

Tous ces fichiers sont des fichiers textes. Nous pouvons donc les lire, les écrire et les modifier avec n’importe quel éditeur de texte. Mais :

* sous Windows, l’éditeur de texte par défaut corrompt l’encodage des fichiers texte (i.e. ces fichiers seront difficilement utilisables par d’autres logiciels, et leur utilisation renverra des erreurs pénibles à corriger) ; Nous déconseillons très fortement de l’utiliser…
* tous ces fichiers contiennent des mots clefs spécifiques (« commandes ») de Therion. Un éditeur qui permet la coloration syntaxique (i.e. qui va reconnaître et colorer les mots clefs spécifiques Therion) va grandement faciliter la lecture et l’édition de ces fichiers.

![Example](/assets/images/Coloration-syntaxe-1290x1024.png)

<p style="text-align:center;"><i>
Exemple d’un fichier de compilation ouvert dans un éditeur de texte (ici BBEdit) avec coloration syntaxique : les commandes sont en bleu, les commentaires en mauve, les chaînes de caractères en rouge, les nombres en orange,… Sur le côté, nous avons les numéros de lignes, et dans cet exemple là, le triangle noir ligne 27 indique que le bloc du layout xviexport a été rétréci pour accéder plus rapidement à la suite.</i></p>

Installer un vrai éditeur de texte n’est pas obligatoire, parce que XTherion contient son propre éditeur de texte, mais pour l’instant, aucune coloration syntaxique n’est disponible. Voici donc quelques propositions qui peuvent être utiles.

Les utilisateurs de Windows doivent faire très attention : Sous Windows, la gestion de l’encodage des caractères et des fins de lignes n’est vraiment pas simple à faire. Si vous avez des problèmes de compilation de fichiers édités avec un éditeur externe, et que vous ne comprenez pas pourquoi la ligne indiquée comme problématique est effectivement problématique (généralement en début de fichier), c’est que très probablement votre encodage est corrompu. En ce cas, le meilleur conseil est peut-être de travailler avec l’éditeur intégré à XTherion.

# Notepad++

Sous Windows, un des meilleurs éditeurs de texte libre est le logiciel [NotePad++](https://notepad-plus-plus.org/).

## Customiser NotePad++

Pour que NotePadd++ puisse travailler correctement avec les fichiers Therion :

1. Aller dans le menu « Settings »
1. Cliquer sur « Preferences »
1. Dans la boite de dialogue qui s’ouvre, séléctionner l’onglet « New Document »
1. Activer le bouton « UTF-8 without ROM »
1. Puis cliquer sur « Apply to open ANSI file »

## Définir le style de langage Therion pour NotePad++

Télécharger le fichier de définition de langage : https://therion.speleo.sk/wiki/_media/contrib:userdefinelang-survextherion533-.zip et le dézipper dans le dossier `%APPDATA%\Notepad++`.

D’autres informations sont disponibles (en anglais) sur la [doc Therion en ligne](https://therion.speleo.sk/wiki/contrib:externaleditors#notepad).

# Visual Studio Code (Microsoft) / VSCodium (Libre)

Récemment un éditeur de texte dédié au code et gratuit a été publié par Microsoft : [Visual Studio Code](https://code.visualstudio.com/). C’est multiplateforme (Windows, MacOS, Unix), il existe de nombreux plugins, mais le seul problème est que ce logiciel est distribué avec des trackers. Mais, le code source de ce logiciel a été mis en ligne, et un équivalent libre sans tracker a été ensuite publié : [VSCodium](https://vscodium.com/). Il est toujours multi-OS.

La force de ce logiciel, est que c’est plus qu’un simple éditeur de texte/code, par exemple :

1. Il existe un plugin spécifique au language Therion, [vscode-therion-language](https://marketplace.visualstudio.com/items?itemName=rhystyers.therion), avec complétion, coloration syntaxique des mots clefs, compilation, quelques commandes utiles spécifique Therion,… Pour l’installer, télécharger l’extension, puis installez là à partir de VSCodium.
1. La possibilité de travailler fichier à fichier, où sous forme de de projet,
1. La possibilité d’interagir avec un dépôt Git,
1. La présence d’un Terminal permettant notamment de compiler les thconfig édités !
1. Et plein d’autres truc sympas…

# BBEdit

La version gratuite de [BBEdit](https://www.barebones.com/products/bbedit/) fonctionne bien avec les fichiers Therion sous MacOS.

Xavier a écrit des fichiers de configuration (à améliorer) pour la syntaxe Therion. Ils sont disponibles avec la procédure d’installation associée sur https://github.com/robertxa/Therion-TextWrangler.

# Brackets

[Brackets](http://brackets.io/) est un logiciel libre pour MacOS, Windows et Linux

Xavier a écrit des fichiers de configuration (à améliorer) pour la syntaxe Therion. Ils sont disponibles avec la procédure d’installation associée sur https://github.com/robertxa/Therion-Brackets.

# KatePart (Kate, KWrite)

C’est un logiciel libre pour Linux. La coloration syntaxique pour les fichiers Therion se trouve sur https://therion.speleo.sk/wiki/_media/contrib:katetherion.zip

# Emacs

Pour les habitués à ce logiciel, une coloration Syntaxique Therion pour ce logiciel est disponible (avec les instructions d’installation) : https://therion.speleo.sk/wiki/_media/contrib:therion-emacs.zip

# Vi – Vim

Encore pour les habitués, il est possible d’utiliser Vi ou Vim pour travailler avec les fichiers Therion. La coloration syntaxique peut être installée à partir de https://therion.speleo.sk/wiki/_media/contrib:therion-vim.zip

 
Plus d’informations se trouve sur la page dédiée du [Wiki Therion](https://therion.speleo.sk/wiki/contrib:externaleditors)
