---
title: Installer la suite Therion
layout: page
---

# Télécharger le logiciel

Pour installer la suite **Therion**, il faut télécharger le logiciel (ou les sources, dépendemment de votre système d’exploitation) sur la page https://therion.speleo.sk/download.php.

# Installation sous Windows

L’installation est simple, il suffit d’exécuter le fichier d’install, et de suivre les instructions. Toutes les dépendances nécessaires au bon fonctionnement des logiciels de la suite Therion sont installées automatiquement.

# Installation sous MacOS

Sous MacOS, l’installation est un peu plus complexe parce qu’il faut 1) installer les dépendances nécessaires au bon fonctionnement de Therion, et 2) compiler les sources Therion.

Pour cela, si ce n’est pas déjà fait, vous avez besoin d’installer :

- **Xcode** à partir de l’AppStore (être patient, c’est long à télécharger et installer)
- **Command Line Tools** (outils de commandes en ligne) : Dans Xcode aller dans Xcode → Preferences → Downloads (Téléchargement) → Command Line Tools (Outils de commandes en ligne)
- Le gestionnaire de Packages [Homebrew](https://brew.sh/index_fr). Pour cela, copier la ligne suivante dans le Terminal (voir utilisation plus bas), et taper « entrer » :

    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
    ```

# Installer les dépendances

1. Ouvrir une fenêtre Terminal (Pour la trouver, aller dans le Launchpad, et dans la barre de recherche, taper « **Terminal** »)
2. Mettre à jour la base de données d’Homebrew en tapant dans le terminal :

    ```bash
    brew update
    brew doctor
    ```
    
    Suivre les instructions issues de brew doctor s’il y en a, et si besoin mettre à jour les application avec la commande : `brew upgrade`

3. Installer les dépendance :
    - Installer la suite MacTeX (tout ce qui touche au langage TeX, LaTeX et pdfTeX)) à partir du site https://www.tug.org/mactex/

    - Installer quelques outils supplémentaires requis par Therion:

    ```bash
    brew install lcdf-typetools
    brew install wxmac
    brew install freetype
    brew install vtk
    brew install --overwrite imagemagick
    brew doctor
    ```

L’option « –overwrite » permet d’éviter les conflits avec les bibliothèques d’XCode qui sont simplifiées et qui ne contiennent pas toutes les bibliothèques nécessaires.

# Compiler Therion

1. Décompresser l'archive `therion-5.*.tar.gz`
2. Ouvrir une fenêtre **Terminal** (Pour la trouver, aller dans le Launchpad, et dans la barre de recherche, taper « **Terminal** »)
3. Dans le terminal, aller dans le dossier avec la commande « cd » en tapant :

    ```bash
    cd chemin/vers/le/dossier
    ```

4. taper ensuite (certaines étapes sont longues, ne pas s’inquiéter) :

    ```bash
    make config-macosx
    make
    sudo make install
    ```

# Erreurs possibles

Dépendamment du système utilisé, Il est possible que le démarrage de l’application XTherion ou Loch indique une erreur disant qu’il ne trouve pas la bibliothèque BWidget :

	`Error in startup script: can't find package BWidget`

Dans ce cas, il faut :

Télécharger la librairie BWidget sur : https://sourceforge.net/projects/tcllib/files/BWidget/

Décompresser et copier la librairie BWidget dans le dossier lib/ de tcl-tk (normalement dans /usr/local/opt/tcl-tk/lib)

Modifier le fichier .profile du terminal :

1. Ouvrir une fenêtre Terminal
2. Taper « cd » puis la touche « Entrer »
3. Taper « open .profile ». Ca devrait ouvrir dans TextEdit un fichier qui s’appelle .profile (c’est normalement un fichier caché)
4. Dans le fichier .profile, copier (et peut-être adapter en fonction de votre système) les lignes

    ```bash
    export PATH="/usr/local/opt/tcl-tk/bin:$PATH"
    export LDFLAGS="-L/usr/local/opt/tcl-tk/lib"
    export CPPFLAGS="-I/usr/local/opt/tcl-tk/include"
    export PKG_CONFIG_PATH="/usr/local/opt/tcl-tk/lib/pkgconfig"
    ```

Attention aussi, lors des mises à jour majeures du package VTK, il faut recompiler les sources, sinon, Loch ne fonctionnera plus.
Installation sous Linux

Voir la [documentation en ligne](https://therion.speleo.sk/wiki/doku.php) et le [ThBook.pdf](http://therion.speleo.sk/downloads/thbook.pdf).
