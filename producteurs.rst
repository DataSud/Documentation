==================
Espace producteurs
==================


Ce guide est destiné aux Producteurs de données sur DataSud : https://publier.datasud.fr/ 

.. note:: Toute personne, morale ou physique, publique ou privée, peut contribuer à la Plateforme, en publiant des jeux de données,  des textes, des ressources et des commentaires. Un Utilisateur peut demander et obtenir le statut de Contributeur et Référent pour une organisation

-----------------------------------------------------------------------------
Devenir Contributeur sur DataSud pour une organisation
-----------------------------------------------------------------------------

Un producteur de donnée qui souhaite les publier sur DataSud doit nécessairement s'inscrire : https://publier.datasud.fr comme les Utilisateurs (voir Espace Utilisateur)

Toute personne inscrite sur la plateforme en tant qu’Utilisateur peut créer une nouvelle organisation ou demander et obtenir le statut de Contributeur pour une organisation déjà existante. 

Ces organisations sont le plus souvent des personnes morales (autorités administratives, associations, entreprises) mais également des groupes informels.

.. image:: CaptureDataSudFirstConnect.PNG

.. image:: 

**Le Contributeur dispose des fonctionnalités suivantes :**

* publier un Jeu de données et y ajouter des Ressources, sous la forme d’un fichier téléchargeable, d’un lien ou d’une API,
* accorder le niveau d'accès aux ressources et jeux de données qu'il a crée pour son organisation : il peut les rendre soit accessible à tous, soit uniquement aux Utilisateurs inscrits, soit les restreindre à un Utilisateur, une Organisation ou uniquement l’Organisation propriétaire du Jeu de données.

**Le Référent dispose des fonctionnalités suivantes :**
* éditer ou supprimer un Jeu de Données publié par un Contributeur de l’Organisation dont il est Référent
* accorder le niveau d'accès aux ressources et jeux de données de toutes les données de son organisation, y compris ceux qu'il n'a pas crée. Il est le référent pour l'ensemble des données de son organisation.
* éditer ou supprimer un statut de Membre ou de Contributeur d’un Utilisateur d’une Organisation à laquelle il appartient

------------------------------------------
Comment devenir Contributeur et Réferent ?
------------------------------------------

.. note:: La demande de **création d'une nouvelle organisation doit se faire au moment de l'inscription individuelle**.

- Lors de la création de son compte Utilisateur, il est possible de se rattacher à une Organisation ou non.
- Demander de devenir Contributeur et Référent peut se faire au moment de son inscription pour une nouvelle organisation ou après l'inscription si l'organisation est déjà existante sur DataSud.
Etape n°1 :- Les demandes de statut de Contributeur ou de Référent sont soumis à la validation des Administrateurs *à priori*. Il faut donc patientier un peu. 

*Les Administrateurs de la Plateforme se réservent la possibilité de révoquer une inscription, un statut de Contributeur ou de Référent, sans avis préalable.*

----------------------------------------------
Publier un jeu de données
----------------------------------------------

*- Pour publier un jeu de donner le Contributeur doit être connecté à l'espace d'administration DATASUD https://publier.datasud.fr
- Pour retrouver ses organisations le Contributeur doit cliquer sur l'onglet *mes organisations* dans son espace d'administration. 

.. image:: les_organisations.PNG


.. note:: La publication se fait en deux étapes : renseigner les métadonnées de son Jeu de Données (dataset) et publier une ou plusieurs Ressources.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Etape n°1 : Renseigner les métadonnées
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: CaptureDataSudAddDataset.PNG

**Les métadonnées obligatoires sont les suivantes :**

- Titre
- Organisation
- Descriptif
- Licence
- Dates (par défaut)

.. note:: le descriptif est un champ incontournable pour garantir une bonne réutilisation. N'oubliez pas, une donnée bien décrite est une donnée bien réutilisée ! ::

Les métadonnées facultatives sont les suivantes :

- Thématiques
- Mots-clés
- Type de données
- Meta-données INSPIRE
- Fréquence de mise à jour
- Couverture régionale


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Etape n°2 : Publier une ressource
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Il existe trois manières d'ajouter un jeu de données :

.. image:: CaptureDataSudAddResource.PNG

1.	Téléverser un fichier : soit par téléversement manuel d'un jeu de donnée depuis votre poste local. La ressource s’ajoute dans l’entrepôt de données DataSud ;
2.	Télécharger depuis une URL : soit en indiquant une URL de téléchargement d'un jeu de donnée depuis une URL. Datasud va alors chercher la ressource pour la télécharger et l'ajouter dans l’entrepôt de données ; 
3.	Référencer une URL ! soit en référençant une URL. La ressource n'est alors pas téléchargée dans DATASUD mais vous indiquez où elle peut être téléchargée. Le catalogue indique où télécharger la donnée chez le Producteur.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Synchroniser une ressource distante
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Si vous choisissez le téléchargement par URL distante (option 2 ci-dessus), vous avez la possibilité de synchroniser votre donnée, selon une périodicité à indiquer.
Datasud va alors chercher la ressource pour la télécharger et l'ajouter dans l’entrepôt de données au pas de temps donnée (tous les jours à tous les ans).

.. image:: CaptureDataSudAddResourceSync.PNG

Par exemple, vous indiquer l'URL de téléchargement un fichier transport.zip que vous souhaitez synchroniser tous les mois sur DATASUD. 

.. note:: Quelques précautions pour que la synchronisation s'active : 
* votre fichier doit avoir **exactement** le même nom de fichier pour toute la synchronisation : si un script modifie le nom de fichiers, pour rajouter une date ou autre par exemple, la synchronisation ne fonctionnera pas.  ;
* votre fichier doit être accessible par DATASUD sur une URL fixe : évitez les liens temporaires.::

En cas d'erreur, les Administrateurs de DATASUD se chargeront de vous indiquer que la synchronisation ne fonctionne pas ou plus.

--------------------------------------------------
Datastore et données intelligentes
--------------------------------------------------

Datasud propose un **datastore**, c'est à dire un entrepôt de données qui offre un certain niveau de **services dits "intelligents" sur les données (pour l'instant) tabulaires aux formats CSV et XLS**. L'indexation de vos données dans le datastore permet notamment de transformer vos données en données semi-structurées et de :

- visualiser et parcourir ces dernières,
- les filtrer par champs.
- créer des datavisualisations simples,
- automatiser l'accès par API.

Permettre l'accès à vos données par interface de programmation est une condition nécessaire pour massifier, industrialiser les usages qui peuvent être fait de ces dernières. C'est également une exigence de la loi république numérique de diffuser dans un format ouvert et interprétable par une machine. Sur Datasud, le format CSV est le format pivot à privilégier pour transformer vos données tabulaires en données semi-structurées dites "intelligentes". 

**Dans la version bêta de DataSud cette mécanique est encore sensible.**

**Vos jeux de données doivent être préparés pour être proprement indexés dans le datastore :**

- Le format CSV à priviliégier doit privilégié avec un ; comme séparateur / délimiteur.
- Idéalement, passez tous vos jeux de données en UTF-8. Notepad++ fait cela très bien.
- Idéalement, exportez vos tableurs favoris (Microsoft, Libre et Open Office) au format CSV.
- Restreindre vos titres de colonnes à moins de 62 caractères.
- En théorie les caractères spéciaux ('\:.,( -') sont acceptés, les éviter dans les titres c'est beaucoup mieux.
- Harmoniser le type de vos données (et oui vos données sont typées) : en effet si une colonne ne comporte que des chiffres, le Datastore autodéterminera le type de cette colonne comme étant un nombre. Or si une valeur contient l'entrée N/A, le datastore va générer une erreur. Pour eviter les erreurs de type, une solution amont à l'indexation consiste à soit corriger les erreurs, soit transformer toutes vos cellules en cellules au format TEXTE. Cela n'est pas satisfaisant, mais ca fonctionne.

Utilisez des outils appropriés pour nettoyer vos données :

- La méthode infolabs, produire un CSV de qualité : http://infolabs.io/prod-csv 
- Les outils http://csvlint.io/ https://goodtables.io/ ou http://openrefine.org/

**Attention :**

- EXCEL : seule la dernière feuille de calcul (ou onglet) est indexée dans le datastore. Il est donc nécessaire de déplacer la feuille de calcul qui contient les données que vous voulez indexer dans le datastore en dernière place de votre classeur.

- EXCEL : si vous ne voulez pas indexer vos données dans le datastore (pour plein de bonnes et mauvaises raisons), il suffit d'ajouter une feuille de calcul vide en dernière, à la fin du classeur. 

- ERREUR : En cas d'erreur supprimez complètement la ressource associée au jeu de données et ajoutez en une nouvelle.

- Les données indexées dans le datastore sont ensuite "requetables" directement à travers l'API à travers une série de fonctionnalités puissantes. Présentation de l'API CKan :

http://datasud.readthedocs.io/fr/latest/developpeurs/index.html#service-api-ckan

--------------------------------------------------
Règles de nommage de vos ressources
--------------------------------------------------

Inspirer des recommandations en matière de nommage des fichiers électroniques et de plan de classement, nous vous proposons de respecter les règles suivantes relatives aux intitulés des ressources (fichiers) associées à vos jeux de données :


- Le nom d’un fichier doit être succinct : éviter de dépasser 30 caractères (sans compter l’extension).
- Le nom d’un fichier doit être précis : il contiendra idéalement : le sujet, le type de document, la date de création, éventuellement la version.


- Date: pour le 20 décembre 2016 => 20161220 (norme ISO 8601).
- Ne pas utiliser des mots vides : le, la, les, de, etc.
- Préférer le caractère _(underscore, tiret du 8) à un espace
- Eviter les lettres accentuées
- Le nom d’un fichier ne doit pas contenir : espace, ponctuation (sauf le point avant l’extension), caractères accentués ou spéciaux (ùé+’@à°[] :</* »& !$, etc.).
- La gestion des versions permet de suivre l’évolution et les étapes de l’élaboration d’un fichier. Il faut les distinguer soigneusement en les numérotant pour obtenir une suite logique exemple V01, V02, etc.

-----------------------------------------------------
Géolocalisation de vos données tabulaires (XLS et CSV)
------------------------------------------------------

Une carte peut automatiquement être générée à partir de vos données tabulaires geolocalisées. Pour cela vous devez intulité vos deux colonnes "latitude" et "longitude".

Projections : en cours de rédaction.

--------------------------------------------------
Amélioration des champs descriptifs avec Markdown
--------------------------------------------------

Pour les champs descriptifs de vos jeux de données et de vos ressources et de vos organisations vous pouvez utiliser la syntaxe Markdown.

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

-------------------------------------------------------
Renseigner les métadonnées INSPIRE
-------------------------------------------------------

Cette partie de la documentation est en cours de rédaction.


