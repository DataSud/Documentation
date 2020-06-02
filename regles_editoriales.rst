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

Vous pouvez afficher une image dans vos descriptifs. Attention, la taille n'est pas paramétrable et l'image doit déjà être disponible en ligne quelque part ::

   .. image:: CaptureDataSudConnect.PNG


.. image:: CaptureDataSudConnect.PNG


=== Liens ===

Pour créer des liens ::

   [texte du lien](url_du_lien "texte pour le titre, facultatif")
   https://trouver.datasud.fr (automatique si mon url commence par http ou https).

[Trouver des données sur Datasud.fr](https://trouver.datasud.fr)

 
=== Aller plus loin ===

https://fr.wikipedia.org/wiki/Markdown

https://guides.github.com/features/mastering-markdown/

https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf


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
