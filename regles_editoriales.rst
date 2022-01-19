==================
Régles éditoriales
==================

--------------------------------
Règles de nommage des ressources 
--------------------------------

Selon les recommandations en matière de nommage des fichiers électroniques et de plan de classement, nous vous proposons de respecter les règles suivantes relatives aux intitulés des ressources (fichiers) associées à vos jeux de données :

- Le nom d’un fichier doit être succinct : éviter de dépasser 30 caractères (sans compter l’extension).
- Le nom d’un fichier doit être précis : il contiendra idéalement : le nom du producteur, le sujet, le type de document, la date de création, éventuellement la version.

- Date: pour le 20 décembre 2018 => 20181220 (norme ISO 8601).
- Ne pas utiliser des articles ou mots vides : le, la, les, de, etc...
- Préférer le caractère _(underscore, tiret du 8) à un espace
- Eviter les lettres accentuées
- Le nom d’un fichier ne doit pas contenir : espace, ponctuation (sauf le point avant l’extension), caractères accentués ou spéciaux (ùé+’@à°[] :</* »& !$, etc.).
- La gestion des versions permet de suivre l’évolution et les étapes de l’élaboration d’un fichier. Il faut les distinguer soigneusement en les numérotant pour obtenir une suite logique exemple V01, V02, etc.

------------------------------------------------------------
Amélioration des champs descriptifs avec le langage Markdown
------------------------------------------------------------

Pour les champs descriptifs des jeux de données, des ressources et des organisations vous pouvez utiliser le langage Markdown dans le but est d'offrir une syntaxe facile à lire et à écrire.

Voici quelques exemples de syntaxe Markdown.

Cette liste n'est pas exhaustive.

=== Formatage ===

Mettre du texte en italique ::

    *quelques mots*

*quelques mots*

Mettre du texte en gras ::

    **plus important**

**plus important**


Pour mettre du code dans le texte::

    ``Mon code``

``Mon code``

=== Listes ===

Sauter une ligne avant le début de la liste.

Pour créer une liste non ordonnée ::

   * Pommes
   * Poires
   

* Pommes
* Poires  

=== Image ====

Vous pouvez afficher une image dans vos descriptifs :


.. image:: CaptureDataSudConnect.PNG

Voici la syntaxe à écrire ![40% center](Image.jpg)

! indique une image à insérer

Entre crochets on trouve les options réduction ou agrandissement en pourcentage et centrage (center). 
Par défaut l'image est alignée à  gauche en taille 100%

**Attention** L'image doit être disponible en ligne quelque part.

=== Liens ===

Pour créer des liens ::

   [texte du lien](url_du_lien "texte pour le titre, facultatif")
   https://trouver.datasud.fr (automatique si mon url commence par http ou https).

[Trouver des données sur Datasud.fr](https://trouver.datasud.fr)

 
=== Aller plus loin ===

https://fr.wikipedia.org/wiki/Markdown

https://guides.github.com/features/mastering-markdown/

https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf

Le guide du Markdown, par YannHY 
https://github.com/YannHY/cours/blob/master/Markdown/Le%20guide%20du%20Markdown.md

-----------------------------------
Datastore et données intelligentes
-----------------------------------

Datasud propose un **datastore**, c'est à dire un entrepôt de données qui offre des **services dits "intelligents" sur les données tabulaires aux formats CSV, XLS, GeoJSON, SHP**.

La publication des données sur Datasud, dans un format ouvert et interprétable par une machine, permet leur indexation dans le datastore afin notamment de proposer des apercus, de les filtrer par champs et de les parcourir sans utiliser de tableur dédiés.

Le format CSV est le format pivot à privilégier pour transformer vos données tabulaires en données semi-structurées dites "intelligentes" afin que le datastore génère des datavisualisations simples sous forme de grille, de graphe ou de carte.

Des données intelligentes permettent également d'en automatiser l'accès par API ( Application Programming Interface) : 
L'accessibilité des données par interface de programmation est une condition nécessaire pour massifier et industrialiser les usages qui peuvent être fait de ces dernières. 
Les données indexées dans le datastore sont ensuite "requetables" directement à travers l'API à travers une série de fonctionnalités puissantes. 
( voir la présentation de l'API CKan : http://datasud.readthedocs.io/fr/latest/developpeurs/index.html#service-api-ckan)

**Vos jeux de données doivent être préparés pour être proprement indexés dans le datastore :**

* Dans CKAN, le format CSV doit être privilégié avec une virgule  **,** comme séparateur / délimiteur.
* Idéalement, passez tous vos jeux de données en UTF-8. Pour cela le programme Notepad++ fait cela très bien.
* Idéalement, exportez vos tableurs favoris (Microsoft, Libre et Open Office) au format CSV.
* Restreindre vos titres de colonnes à moins de 62 caractères.
* Ne pas doublonner le titre d'une colonne.
* En théorie les caractères spéciaux ('\:.,( -') sont acceptés, mais c'est beaucoup mieux de les éviter dans les titres.
* Harmoniser le type de vos données (et oui vos données sont typées!) : en effet si une colonne ne comporte que des chiffres, le datastore autodéterminera le type de cette colonne comme étant un nombre. Or il suffit qu'une cellule de la colonne contienne l'entrée N/A, pour que le datastore génére une erreur. 
Pour éviter les erreurs de type, il est préférable de les corriger avant d'indexer le jeu de donnée dans DataSud ou bien de transformer la valeur des cellules en cellules au format TEXTE. Cela n'est pas satisfaisant, mais ca fonctionne.

* ERREUR : En cas d'erreur supprimez complètement la ressource associée au jeu de données et ajoutez en une nouvelle.

.. Note:: **Attention avec Excel** Lorque le fichier contient plusieurs feuillet (ou onglet), seule la dernière feuille de calcul est indexée dans le datastore. Il est donc nécessaire de déplacer la feuille de calcul contenant les données que vous souhaitez indexer dans le datastore en dernière place de votre tableur. Si vous ne voulez pas indexer vos données dans le datastore (pour plein de bonnes et mauvaises raisons), il suffit d'ajouter une feuille de calcul vide en dernière place de votre tableur.::


--------------------------------------
Les outils pour nettoyer vos données 
--------------------------------------


`La méthode infolabs pour produire un CSV de qualité <http://infolabs.io/prod-csv>`_

`Outil de validation des données ouvertes Validata <https://validata.fr/>`_

`Nettoyer les CSV avec CSVLint (en Anglais) <http://csvlint.io>`_

https://goodtables.io/ 

http://openrefine.org/

----------------------------------------------
Les guides et outils de production des données
----------------------------------------------

Si vous débutez en matière de réutilisation de données publiques, ouvertes, personnelles, sensibles, géographiques, etc.. nous vous invitons à commencer par découvrir la documentation produite par l'association OpenDataFrance :

`Ressources Opendatalocale <http://opendatalocale.net/ressources>`_

`D-lyne Outil de production des données respectant les standards existants, développé par OpendataFrance : <http://d-lyne.fr/portail/login.php>`_

- Saisie assistée
- Contrôle de la qualité
- Standardisation
- Export et publication open data
- Base de production permanente

`Les Guides d'Etalab <https://guides.etalab.gouv.fr/>`_ ont pour objectif de vous accompagner à améliorer la qualité de vos productions, collectes ou utilisation des données, codes sources de logiciel ou algorithmes :

#L'ouverture et la circulation des données : 

- Comment préparer des données à l'ouverture / la circulation ?
- Quels jeux de données doivent être publiés en open data ?
- Comment publier des jeux de données sur data.gouv.fr ?
- Pourquoi et comment créer un schéma de données ?
- Comment utiliser l'IA pour pseudonymiser des documents ?

#La transparence des algorithmes publics

- Les algorithmes publics : pourquoi et comment les expliquer ?

#L'ouverture des codes sources de logiciels

- Codes sources du secteur public : lesquels ouvrir, pourquoi et comment ?


`Module de eLearning proposé par le portail européen de l’OpenData <https://www.europeandataportal.eu/elearning/fr/#/id/co-01>`_
