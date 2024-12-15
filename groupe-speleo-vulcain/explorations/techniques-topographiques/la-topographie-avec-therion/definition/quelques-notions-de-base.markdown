---
title: Quelques notions de base
layout: page
---

Avant de pouvoir entrer dans le vif du sujet, il est nécessaire de rappeler quelques notions de base. Elles ne sont pas difficile (en tout cas, pas plus que d’aligner 3 ou 4 mots cohérents !), mais elles sont indispensables à comprendre et à intégrer.

Comme nous l’avons décrit plus tôt, tous les fichiers d’entrées sont des fichiers textes. Nous pouvons donc les créer, les lire et les modifier avec n’importe quel éditeur de texte. Voila quelques règles de base qui vous évitera de nombreux problèmes :

# De l’utilisation des noms (de fichiers, de topographies,…)

**Les noms des fichiers textes ne doivent comporter ni d’espace, ni de caractères accentués**. Idéalement, leurs noms sont représentatifs de ce qu’ils sont.

Idem, ne pas utiliser d’espace ou de caractères accentué dans les noms des identifiants que nous utiliserons tout au long de la topographie.

# Le séparateur de décimales

C’est un problème. Dans les langues latines, comme le français, le séparateur de décimales est la virgule. Si vous avez acheté votre ordinateur en France et que vous n’avez pas modifié les paramètres régionaux et la définition du séparateur de décimales, alors, certains (rares) programmes vont considérer que la décimale est bien marquée par une virgule. C’est le cas, par exemple, du logiciel Microsoft Excel, qui est souvent utiliser pour entrer des données topographiques.

Mais voilà, dans les langues anglo-saxonnes, le séparateur de décimales, c’est le point et non la virgule. Et par défaut, la plupart des logiciels (sauf de rares exceptions comme Microsoft Excel) travaillent en convention anglo-saxonne, c’est à dire avec le point. C’est le cas de Therion, mais aussi de la plupart des logiciels SIG.

En conséquences, si vous faites un copier-coller de votre tableau de données Excel avec une virgule comme séparateur de décimales, dans un fichier pour Therion, et bien, vous allez recevoir une belle volée d’insultes.

Alors, faites attention à comment vous séparer vos décimales…

Un moyen très simple de s’affranchir de ce problème, c’est de modifier les préférences de votre système, et d’imposer le point comme séparateur de décimales. C’est simple à faire, et ça évite beaucoup d’erreurs… et de prises de tête…

# Des mots clefs de commandes

Dans ces fichiers textes, chaque ligne va correspondre à une commande donnée par un mot clef correspondant à cette commande. Chaque ligne sera donc exécutée lors de la compilation.

Nous devons écrire une commande par ligne. Ne pas écrire plusieurs commandes sur la même ligne.

Quelque soit le fichier, chaque information que nous voulons donner est écrite sous la forme : « **commande » <attributs> [-options <attributs de l’option>]**. Par exemple, si nous voulons définir « Monsieur Vulcain » comme auteur d’une topographie, la « commande » est le mot « team » et l’attribut est « Monsieur Vulcain ». Nous écrirons dans le bloc d’une séance topographique :

	team "Monsieur Vulcain"

Nous ne pouvons pas écrire juste « team » sans l’attribut parce que es attributs sont obligatoires.

En revanche, les options ne sont pas obligatoires. Si ce Monsieur Vulcain a été la personne à la prise de note et que nous voulons l’indiquer dans les données, nous écrirons :

	team "Monsieur Vulcain" notes

« notes » est le mot clef spécifique de cette information.

Ceci n’est qu’un exemple, et permet d’illustrer comment nous allons écrire les informations dans les fichiers d’entrées de Therion. Toutes les commandes fonctionnent de manière identiques. Seul le nombre d’attributs et le nombre d’options change.

Il faut noter que toutes les commandes sont des mots clefs anglais. Mais généralement, ce sont des mots que vous connaissez déjà parce que vous les avez déjà vus par ailleurs. Dans la suite, pour chaque mots clef ou commande utilisé, nous essayerons d’en donner la traduction française pour faciliter l’apprentissage.

# Comment rajouter un commentaire ?

Si nous souhaitons ajouter un commentaire (par exemple pour expliquer ce que fait tel ou tel ligne, ou pour qu’une ligne ne soit pas exécutée temporairement), nous pouvons commenter cette ligne. Il suffit alors d’ajouter le caractère dièse « # » au début de la ligne.

Par exemple :

	Cette ligne n'est pas un commentaire et va générer une erreur car elle n'est pas une commande non plus

	# Cette ligne, en revanche, et bien un commentaire, parce qu'elle est précédée d'un "#"
	# Pour continuer un commentaire sur la ligne suivante, il faut de nouveau commencer la ligne avec le signe "#"

# La notion de blocs

Nous allons voir que la structure de tous ces fichiers est basée sur **des définitions de blocs** :

- des blocs de topographies (fichiers de données),
- des blocs de séances topographiques (fichiers de données),
- des blocs de mise en page (fichiers de compilation et de configuration),
- des blocs de calques (fichiers de dessin),
- des blocs de lignes (fichiers de dessin),
- des blocs d’aires (fichiers de dessin),
- des blocs de maps (fichiers de données ou de liaisons de données).

Il nous faut apprendre à définir des blocs. Définir un bloc, ce n’est pas difficile, il faut lui dire où il commence, et où il finit. Chaque type de blocs est identifié par un nom spécifique. Pour les fichiers de données, nous utiliserons :

- le bloc topographie, qui se nomme le bloc **survey** [=topographie] (fichiers de données),
- le bloc séance topographique, qui se nomme le bloc **centerline** [=ligne centrale/principale] (fichiers de données),
- le bloc de maps qui se nomme **map** [=carte] (fichiers de données ou de liaisons de données).

Pour le dessin, il y a aussi les blocs :

- de scraps : **scrap**
- de ligne : **line**
- d’aires : **area**

Dans les fichiers de configuration et de compilation, nous trouverons le bloc de mise en page (layout en anglais): layout.

Un bloc sera donc défini au début par le mot clef le définissant, et à la fin par le mot « **end** » précédent le mot clef (sans espace). Cela donnera par exemple :

	```
	survey
	   Commandes du bloc survey
	   centerline
	       Commandes du bloc centerline (une séance topographique)
	   endcenterline
	   centerline
	       Commandes du bloc centerline (une autre séance topographique)
	   endcenterline 
	endsurvey
	```

Ce n’est pas obligatoire, mais une bonne chose est de marquer avec une indentation (quelques espaces ou une tabulation) ce qui est à l’intérieur d’un bloc. A chaque bloc imbriqué, nous augmentons alors d’une indentation.
