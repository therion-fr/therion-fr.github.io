---
title: De quoi a besoin Therion?
layout: page
---

Basiquement, Therion a besoin de différents types de fichiers pour pouvoir produire des topographies. Nous verrons plus tard comment les produire, mais voila déjà une première description de ces fichiers.

Des templates d’exemples sont disponibles sur https://github.com/robertxa/Th-Config-Xav/tree/master/Template_cave. Ils peuvent être utilisés pour faciliter le travail.

# Les fichiers de données (extension .th)

Les fichiers de données sont les fichiers qui vont contenir toutes les données brutes de la topographie :

- le nom de la topographie
- la définition des entrées et leurs coordonnées
- Les différentes séances topographiques, avec pour chaque séance :
	- les dates d’exploration et de topographie
	- les auteurs des explorations et des topographies
	- la définition des instruments utilisés pour la topographie, leurs unités et leur calibration si besoin
	- Le type de données topographiques (points, longueurs, compteurs, azimuth pentes, profondeurs, dimensions,…)
	- Le tableau de données de la séance, qui suit le format défini par le type de données

Par défaut, l’extension des fichiers de données est **.th**.

Dans le cas de cavités complexes et/ou de systèmes karstiques, Certains fichiers .th en contiennent pas de données de séances topos, mais servent à lier les différentes données entre elles. Par exemple, ils permettent d’imposer des jonctions entre deux cavités que nous venons de jonctionner. Nous pouvons donc travailler le dessin de chaque cavité ou de chaque zone explorée de façon indépendante, et de fusionner le tout par la suite grâce à ces fichiers.

Ces fichiers peuvent se construire à partir de rien à l’aide d’un éditeur de texte, ou en adaptant la copie d’un fichier pré-existant, ce qui facilite grandement leur construction.

# Les fichiers de commandes de compilation (extension .thconfig)

La philosophie de Therion n’est pas de dessiner pas une topographie comme sous un logiciel vectoriel classique, en voyant directement le résultat. Au contraire, nous dessinons uniquement des lignes, des points et des aires auxquels nous associons des attributs. Nous utilisons alors une banque de figurés issus de banques homogénéisées officielles (par exemple, la banques UIS) qui correspond au attribut donnés lors du dessin. Nous ne pouvons obtenir une carte finale qu’après la compilation du projet qui va interpréter puis transcrire en figurés les points, lignes, et aires en fonction de leurs attributs.

Pour cette compilation, de nombreuses options sont possibles, dépendamment de notre but :

- Quels fichiers de données, de liaisons, et de dessins voulons-nous utiliser pour la production finale ? Quel fichier MNT ? Quelle image de drappage ?
- Par exemple, si nous voulons produire une carte, quelles sont ses caractéristiques ?
	- Quelle vue (plan, coupe développée, coupe projetée) voulons nous ?
    - Quelle projection géographique ? Quel système de référence ?
    - Quelle échelle ?
    - Quelle langue ?
    - Quelles couleurs ?
    - Quelle banque de figurer utiliser ?
    - Veut-on une grille ? Si oui, de quelle taille ?
    - Veut-on un titre ? Une description ? Une légende des figurés utilisés ? Un copyright ?
- Quel type d’export voulons nous après la compilation ?
    - Une carte finale en plan ? en Coupe développée ? En coupe Projetée ?
    - Un atlas ?
    - Un modèle en 3-D ?
    - Des fichiers intermédiaires pour le dessin ?
    - Un fichier kml qu’on puisse intégrer dans Google Earth ?
    - Des Shapefiles pour utiliser dans un logiciel SIG ?
    - Des listes de synthèses (quelles cavités, quelle spéléométrie, coordonnées des cavités, liste des points d’interrogation,…)
    - La base de données sql du sytème ?
    - Sous quel(s) format(s) ? (pdf, dxf, txt, html,…)

Ces questions ne sont pas exhaustives, ce ne sont que des exemples. Mais justement, un fichier de compilation est là pour permettre d’obtenir un produit final en adéquation avec tout ce questionnement. Beaucoup d’options ont des valeurs par défaut, un fichier de compilation peut donc être très simple. Les fichiers de compilation possède une extension .thconfig.

Comme pour les fichiers de données, ces fichiers peuvent se construire à partir de rien à l’aide d’un éditeur de texte, ou en adaptant la copie d’un fichier pré-existant, ce qui facilite grandement leur construction.

# Les fichiers de dessins (extension .th2)

Les fichiers de dessins peuvent être éditer dans un éditeur de texte pour correction, mais pour les produire, il est nettement plus pratique de le faire à l’aide de l’éditeur de dessin dans le logiciel XTherion.

Ces fichiers de dessins possèdent une extension **.th2**.

Ils vont contenir :

- le squelette de la topographie que nous voulons dessiner (ce n’est pas obligatoire)
- un dessin au format jpg ou gif, avec soit une échelle, soit la position de quelques stations topographiques
- les différents calques (appelés scraps en langage Therion) dessinés
- et les dessins des points, des lignes et des aires, avec leurs attributs respectifs

# Les fichiers intermédiaires (optionnel)

Des fichiers intermédiaires peuvent être produits par la compilation (si nous le demandons, évidemment !). C’est notamment le cas pour les fichiers vectoriels du squelette topographique.

Ces fichiers sont au format **.xvi** (texte, mais spécifiquement pour Therion). Ils possèdent la ligne de cheminement, les stations topographiques, et les dimensions à chaque station topographique (gauche, droite, haut, bas ou les visées d’habillage).

Leur intérêt est que nous pouvons les importer dans un fichier dessin, et les utiliser comme base pour pouvoir dessiner directement sur l’écran. Ils sont très utiles pour définir dans le dessin les stations topographiques, et ainsi ancrer le dessin sur le squelette topographique.

Ce sont des fichiers texte, mais il n’y a aucun intérêt à chercher à les éditer manuellement avec un éditeur de texte.

# Les fichiers de configuration (optionnel)

Enfin, il est possible de construire des fichiers de configuration que nous appellerons dans les fichiers de compilation. Ils peuvent avoir deux intérêts :

- simplifier les fichiers de compilation, et du coup les rendre plus lisible,
- homogénéiser le dessin final de toutes les topographies d’un même système

Ces fichiers fonctionnent comme les fichiers de compilation sans les définitions d’exports. Ils sont au format texte, avec l’extension **.thc**.

Comme pour les fichiers de données ou de compilation, ces fichiers peuvent se construire à partir de rien à l’aide d’un éditeur de texte, ou en adaptant la copie d’un fichier pré-existant, ce qui facilite grandement leur construction.
