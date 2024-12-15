---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: La topographie avec Therion
---

Encore beaucoup de spéléos d’exploration font leurs reports topographiques à l’aide de deux logiciels distincts : le premier (comme le très pratique et convivial [Visual Topo](http://vtopo.free.fr/)) permet de construire le squelette de la topographie et de l’exporter dans un format vectoriel, qui est ensuite importé dans le second logiciel, vectoriel, dit de DAO (comme [Inkscape](https://inkscape.org/fr/) ou Adobe Illustrator), permettant de dessiner autour du squelette. Le logiciel Visual Topo est simple d’utilisation. Le logiciel de DAO demande quant à lui un petit temps de formation pour pouvoir l’utiliser correctement. Cette méthode est adaptée aux cavités simples et à la publication de topographie sans intégration dans un Système d’Information Géographique (SIG).

En revanche, à partir du moment où nous travaillons sur des cavités complexes avec de nombreux bouclages ou sur des systèmes karstiques avec plusieurs cavités, cette méthode devient difficile, voir très difficile à mettre en oeuvre. En effet, ici, chaque dessin est fixe et indépendant de la donnée topographique. Cela pose problème pour connecter deux cavités ou pour ajouter un nouveau réseau/bouclage dans une cavité connue, parce que ce bouclage déforme le squelette, et au bout d’un certain nombre de bouclages, nous n’arrivons plus à relier les dessins de façon acceptable.

C’est pourquoi, des logiciels spécifiques, intégrant à la fois le travail de base sur les données, et le dessin, qui est alors ancré sur le squelette, sont développés depuis quelques années. L’avantage, c’est qu’à chaque nouvel ajout, l’ancien dessin est déformé automatiquement pour coller au nouveau squelette topographique. Cela permet donc l’évolution de la topographie d’une cavité complexe ou d’un système au cours du temps. En France, trois tels logiciels sont connus : [GHTopo](https://ghtopo.blog4ever.com/), [TopoCalc’R](http://topocalcaire.free.fr/) et [Therion](https://therion.speleo.sk/index.php). Therion étant plus ancien et multi-OS (contrairement aux deux autres), nous avions commencé à nous y intéresser avant le développement de TopoCalc’R, et nous y sommes restés. Son avantage est que non seulement il permet ce travail sur la topographie d’une cavité complexe, mais aussi, il permet de travailler de façon robuste à l’échelle d’un système karstique complet.

**Therion**... Arf, rien ne sert de s’enfuir ! Tout le monde a pour idée que c’est un truc de Geeks, que c’est imbitable et difficile à prendre en main. Mais pourtant, **ce n’est pas si compliqué que ça**, du moment que nous prenons le temps de nous y former (et ce n’est pas plus difficile que de se former correctement à un logiciel de dessin vectoriel) et de travailler de façon rigoureuse. Effectivement, si vous êtes allergique à écrire 3 mots consécutifs où à lire un fichier texte, alors, utiliser Therion risque d’être difficile. Mais si vous avez déjà écrit un sms, un e-mail, ou un petit document Word sans mise en page, alors, il n’y a aucune raison que vous n’y arrivez pas, sauf à faire un blocage psychologique ou à y mettre de la mauvaise volonté…

Ces pages ne remplacent pas la pratique et l’expérience, mais elles apportent une base pour l’utilisation rigoureuse de Therion. Ce n’est évidemment pas un tutoriel exhaustif, mais vous trouverez des notions de base, mais aussi des fiches rappels synthétiques qu’il peut être bon de garder sous la main. Cele peut aussi servir à améliorer votre prise de notes sous terre pour pouvoir produire des données qui permettent une meilleure utilisation de Therion.

La description des fichiers peut être rébarbatives, mais il faut en passer par là pour comprendre leur fonctionnement. Par la suite, il sera possible d’utiliser des fichiers plus anciens pour les adapter aux nouvelles topographies, ce qui facilitera la tâche. Il peut être utile d’avoir sous la main des exemples de ces fichiers, afin de les comprendre, et finalement de se rendre compte, que ce n’est pas plus compliqué qu’un texte quelconque, d’autant plus qu’il y a moins de mots 😉

# Préambule

* [Installer la suite Therion](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/preambule/installer-la-suite-therion)
* [Installer un « vrai » éditeur de texte (et sa coloration syntaxique)](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/preambule/installer-un-vrai-editeur-de-texte)
* [Aides Therion disponibles sur le net](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/preambule/aides-therion-disponibles-sur-le-net)

# Qu'est ce Therion? Qu'est ce XTherion?

* [De quoi a besoin Therion?](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/definition/de-quoi-a-besoin-therion)
* [Que peut produire Therion?](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/definition/que-peut-produire-therion)
* [Therion ? XTherion ? Loch ?](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/definition/therion-xtherion-loch)
* [Comment utiliser le logiciel XTherion ?](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/definition/comment-utiliser-le-logiciel-xtherion)
* [Quelques notions de base indispensables](./groupe-speleo-vulcain/explorations/techniques-topographiques/la-topographie-avec-therion/definition/quelques-notions-de-base)

# Entrer des données topographiques pour Therion

* Comment créer un fichier de données ?
* Comment ajouter une nouvelle séance topographique ?

# Créer un fichier de configuration pour la compilation

* Qu'est-ce qu'un fichier .thconfig?
* Compiler ?
* Comment simplifier les fichiers de configuration

# Faire un dessin avec XTherion

- Faire un dessin avec XTherion
- Principaux points utilisés et leurs options classiques
- Principales lignes utilises et leurs options classiques
- Principales aires utilisées et leurs options classiques
- Penser et gérer les calques (= scraps)
- Ajouter un nouveau dessin à la topographie existante
- Ajouter une section de galerie sur un dessin
- Spécificités des coupes développées
- Fiche synthèse des étapes à suivre pour faire un dessin

# Des erreurs classiques

La compilation peut générer des erreurs. Il est important de savoir les repérer, les comprendre et les corriger.

- Comment savoir qu’il y a une erreur ?
- Des erreurs classiques
- Trouver et corriger (débuger) une erreur dans un dessin ?

# Penser « base de données topographiques » et SIG

- La notion de maps
- Structurer une base de données topographiques
- Homogénéiser les topographies à l’aide d’un fichier de configuration global
- Les notions de systèmes de coordonnées et de projections (A améliorer)
- Utiliser un logiciel SIG – principes de base
- Ajouter un Modèle Numérique de Terrain/Surface (MNT) et drapper une image

# Partager la base de données ?

- Comment partager une base de données ?
- Quelle licence utiliser ?
- Quelques exemples…

Contenu créé par Xavier Robert (xavier.robert@ird.fr)

