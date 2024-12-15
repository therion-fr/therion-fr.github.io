---
title: Comment utiliser le logiciel XTherion ?
layout: page
---

Nous pouvons utiliser le logiciel XTherion pour trois actions distinctes :

- effectuer la compilation à partir d’un .thconfig chargé,
- modifier les fichiers Therion (.th, .thconfig,…) dans l’éditeur de texte,
- dessiner une topographie.

Chacune de ces actions s’effectue dans une fenêtre spécifique. A l’ouverture de XTherion, nous obtenons cette fenêtre (ici annotée) :

![Fenêtre de compilation](/assets/images/Therion-fenetre-compil-1477x1024.jpg)
<p style="text-align:center;"><i>Fenêtre de compilation</i></p>

# Fenêtre de compilation

Les trois boutons « **Editeur de texte** », « **Editeur de dessin** » et « **Fenêtre de compilation** » permettent de changer type de fenêtre, dépendamment de ce que nous voulons faire.

Sur toutes les fenêtres, le bouton rond-barré permet de fermer le fichier ouvert dans la-dite fenêtre.

La fenêtre de compilation est divisée en trois parties :

- En haut, une fenêtre d’édition. Lorsqu’un fichier de compilation .thconfig est chargé, il s’affiche ici. Il est alors possible de le modifier. Si nous voulons écrire un nouveau fichier, nous pouvons le faire après avoir appuyé sur le bouton « nouveau ». Nous pouvons alors écrire dans cette fenêtre.
- En bas, une fenêtre vide, dans laquelle nous ne pouvons rien faire. C’est ici que sera affiché tous les informations de la compilation (ce que fait la compilation, les erreurs s’il y en a, les statistiques,…)
- Sur la droite, un panneau de contrôle. Ici, il y a aussi un bouton « compiler » qui fait la même chose de le bouton en forme de roue dentée dans le bandeau supérieur. Lorsqu’on clique sur l’un des deux, si un fichier de compilation .thconfig est chargé, Therion effectue la compilation. A l’issue de la compilation, la case à droite change de couleur. Elle devient verte si la compilation c’est bien passée, elle devient orange s’il y a un warning (c’est à dire qu’il y a une erreur, généralement dans le dessin, mais qu’elle ne plante pas la compilation), et elle devient rouge s’il y a une erreur…

L’éditeur de texte accessible en cliquant sur le bouton adéquat du bandeau se présente quand à lui ainsi :

![L’éditeur de texte intégré à XTherion](./assets/images/Therion-editeur.png)
<p style="text-align:center;"><i>L’éditeur de texte intégré à XTherion</i></p>

Les boutons sont semblables à la fenêtre de compilation. Si besoin, l’action « compiler » est toujours accessible en appuyant sur la roue crantée du bandeau supérieur. A droite, le panneau de contrôle facilite l’entrée de nouvelles données.

Enfin, nous accédons à la fenêtre de dessin en cliquant sur le bouton adéquat du bandeau supérieur. Cette fenêtre est la plus complexe, mais nous la décortiquerons en détail plus tard. Mais son utilisation est très logique, et nous prenons rapidement l’habitude de l’utiliser.

![L’éditeur de dessin](/assets/images/Therion-editeur-dessin.png)
<p style="text-align:center;"><i>L’éditeur de dessin</i></p>

La plus grande partie de l’éditeur de dessin est occupée par l’espace où nous allons dessiner.

Les boutons les plus importants sont ceux du bandeau supérieur à gauche. Ils permettent :

- De créer un nouveau calque (=scrap), des nouveaux points, des nouvelles lignes, des nouvelles aires
- De sélectionner manuellement (la flèche sélection) ou par itération les différents objects du dessin
- De supprimer l’object dessiné.

Le panneau de contrôle contient des onglets :

- de gestion du fichier de dessin (par exemple, ajouter un squelette topographique, ajouter une image de fond, organiser l’ordre des objets,…)
- pour chaque type d’objets (points, ligne, aires) qu’il permet de contrôler (type, sous-type, options,…)

Mis à part un calculateur d’alcoolémie planqué dans l’interface graphique, Il n’y a rien d’autre… Contrairement à la croyance populaire, nous ne pouvons pas dire que ce soit une interface compliquée, loin de là !
