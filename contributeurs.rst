====================
Espace contributeurs
====================


Ce guide est destiné aux producteurs de données, déjà inscrit en tant qu'Utilisateurs https://publier.datasud.fr/ et souhaitant contribuer à l'enrichissement des publications sur la plateforme.
`« voir la documentation sur les Utilisateurs » <https://datasud.readthedocs.io/fr/latest/utilisateurs.html/>`_ 

.. note:: Toute personne, morale ou physique, publique ou privée, producteur de données publiques ou privées peut les publier sur la DataSud, sous reserve d'accepter les « conditions d’utilisation » et de respecter la réglementation sur les données à caractères personnelles.

-----------------------------------------------------------------------------
Devenir Contributeur et Référent pour une organisation
-----------------------------------------------------------------------------

Les organisations sont le plus souvent des personnes morales (autorités administratives, associations, entreprises) ou également des groupes informels.

.. note:: **La création d'une nouvelle organisation peut-être effectuée soit au moment de l'inscription comme utilisateur de DataSud, soit après la validation du profil Utilisateur par les Administrateurs de DataSud**.

.. image:: CaptureDataSudFirstConnect.PNG

Les demandes de statut de Contributeur ou de Référent sont soumises à la validation des Administrateurs de la plateforme.
Il faut donc patienter un peu. 

.. note:: **Par défaut, un Utilisateur qui s'inscrit avec un email personnel (gmail, ymail, hotmail,...) et dont le nom de domaine ne peut correspondre à l'organisation pour laquelle il demande de contribuer, ne peut se rattacher, contribuer ou devenir référent d'une Organisation**

*Les Administrateurs de la Plateforme se réservent la possibilité de révoquer une inscription, une organisation, un statut de Contributeur ou de Référent, sans avis préalable.*


**Un Contributeur dispose des fonctionnalités suivantes :**

* Il peut publier un jeu de données et y ajouter des ressources, sous la forme d’un fichier téléchargeable, d’un lien URL ou d’une API,
* Il peut accorder le niveau d'accès aux ressources et jeux de données qu'il a crée pour son organisation : soit décider de les rendre accessible à tous, soit en restreindre l'accès uniquement à un ou plusieurs Utilisateurs inscrits ou bien à une Organisation choisie comme sa propre Organisation propriétaire du Jeu de données.


**Un Référent des données de l'Organisation, à laquelle il appartient, dispose des fonctionnalités suivantes :**

* Il peut éditer ou supprimer un jeu de données créé et publié par un autre Contributeur de l'Organisation,
* Il peut accorder le niveau d'accès aux ressources et jeux de données de toutes les publications de son Organisation,
* Il peut autoriser ou supprimer le statut de Contributeur aux Utilisateurs,
* Il recoit des notifications lorsque des modifications ont été apportées aux jeux de données et ressources de l'Organisation à laquelle il appartient.

----------------------------------------------
Créer une Organisation
----------------------------------------------

Toute demande de création d'une organisation est soumise à l'administrateur du site pour validation

.. image:: Creation_orga.PNG

La dénomination sociale est obligatoire

.. image:: Creation_orga1.PNG

La description est facultative mais fortement conseillée, d'une part pour permettre de qualifier l'Organisation et sa démarche en matière d'ouverture des données publiques et géographiques et d'autre part pour permettre l'implementation automatique d'une page web spécifique à propos de l'organisation.

.. image:: Creation_orga2.PNG


----------------------------------------------
Editer la page d'une Organisation
----------------------------------------------


Pour éditer la page de son organisation, le Contributeur clique sur l'onglet ORGANISATIONS dans son espace d'administration. 

.. image:: Onglet_organisation.PNG

La première fois que le contributeur édite la page de son organisation, il lui sera demandé de définir le territoire de compétence de l'organisation. La création de ce territoire de compétences permet de bénéficier de fonctionnalités spatiales supplémentaires dans DataSud. Cette demande est traitée par un administrateur du CRIGE.

.. image:: Territoire_competence.PNG

--------------------------
Publier un jeu de données
--------------------------

* Pour publier un jeu de donner le Contributeur se connecte avec son identifiant et mot de passe sur https://publier.datasud.fr

.. image:: InscriptionDataSud.PNG

**La publication se fait en deux étapes successives:** 

Tout d'abord on renseigne les métadonnées servant à définir ou décrire le jeu de données qui sera publié, puis on ajoute des jeux de données brutes ou des ressources complémentaires.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Etape n°1 : Renseigner les métadonnées
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: Edit_newdataset1.PNG

.. note:: De nombreux mots-clés sont déjà répertoriés dans la base. Ils apparaissent dans une liste déroulante lorsque vous saisissez les premières lettres du mot. Mieux vaut choisir un mot clés existant, plutot que d'en choisir un nouveau afin de permettre de relier votre jeu de donnée à d'autres jeux similaires inscrit au catalogue de DataSud.

.. image:: Edit_newdataset2.PNG

.. image:: Edit_newdataset3.PNG

**Les métadonnées obligatoires sont les suivantes :**

- Titre
- Organisation à laquelle est rattaché ce jeu de données
- Descriptif  : C'est est un champ incontournable pour garantir une bonne réutilisation, car une donnée bien décrite est une donnée bien réutilisée !
- Dates (par défaut)
- Licence



**Les métadonnées facultatives sont les suivantes :**

- Thématiques
- Mots-clés
- Type de données
- Meta-données INSPIRE
- Fréquence de mise à jour
- Couverture régionale


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Etape n°2 : Publier une ressource
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il existe trois manières différentes d'ajouter un jeu de données :

.. image:: CaptureDataSudAddResource.PNG

**1.	Téléverser manuellement un fichier depuis votre poste local:** 

Dans ce cas la ressource s’ajoute dans l’entrepôt de données DataSud;
Le nom de votre fichier est automatiquement recopié, cependant il est possible de modifier manuellement le nommage de ce jeu de donnée.

Le format du fichier est automatiquement reconnu par DataSud.

**2.	Télécharger depuis une URL en indiquant une URL de téléchargement du jeu de donnée:**

Dans ce cas, Datasud va télécharger la ressource pour l'ajouter dans l’entrepôt de données; 

.. image:: CaptureDataSudAddResourceSync.PNG

Ce mode de publication permet de synchroniser la ressource distante, selon une périodicité régulière à indiquer : 

* Quotidienne (tous les jours à minuit)
* Hebdomadaire (tous les lundis)
* Bimensuelle (1er et 15 de chaque mois)
* Trimestrielle ( 1er des mois de Janvier, Avril, Juillet et  Octobre)
* Annuelle (1er Janvier)

Par exemple, un fichier transport.zip peut-être synchronisé sur DataSud directement grace à son URL de téléchargement.

.. note:: Quelques précautions à prendre pour que la synchronisation s'active correctement : 

* le nom de votre fichier doit avoir **exactement** le même nommage de fichier pour toute la synchronisation : si un script modifie le nom du fichier (pour rajouter une date ou autre par exemple), la synchronisation ne fonctionnera pas.

* votre fichier doit être accessible via une URL fixe : évitez les liens temporaires.::

En cas d'erreur, les Administrateurs de DATASUD se chargeront de vous indiquer que la synchronisation ne fonctionne pas ou plus.

**3.	Référencer une URL:**

Dans ce cas, la ressource n'est pas téléchargée dans DataSud et vous indiquez précisement l'adresse URL de téléchargement de la donnée. qui reste hebergée chez son producteur. 
Cette donnée apparait au catalogue de DataSud mais elle n'est pas hébergée dans son entrepot.





--------------------------------------------------
Datastore et données intelligentes
--------------------------------------------------

Datasud propose un **datastore**, c'est à dire un entrepôt de données qui offre des **services dits "intelligents" sur les données tabulaires aux formats CSV, XLS, GeoJSON, SHP**.

La publication des données sur Datasud, dans un format ouvert et interprétable par une machine, permet leur indexation dans le datastore afin notamment de proposer des apercus, de les filtrer par champs et de les parcourir sans utiliser de tableur dédiés.

Le format CSV est le format pivot à privilégier pour transformer vos données tabulaires en données semi-structurées dites "intelligentes" afin que le datastore génère des datavisualisations simples sous forme de grille, de graphe ou de carte.

Des données intelligentes permettent également d'en automatiser l'accès par API ( Application Programming Interface) : 
L'accessibilité des données par interface de programmation est une condition nécessaire pour massifier et industrialiser les usages qui peuvent être fait de ces dernières. 
Les données indexées dans le datastore sont ensuite "requetables" directement à travers l'API à travers une série de fonctionnalités puissantes. 
( voir la présentation de l'API CKan : http://datasud.readthedocs.io/fr/latest/developpeurs/index.html#service-api-ckan)

**Vos jeux de données doivent être préparés pour être proprement indexés dans le datastore :**

* Le format CSV doit être privilégié avec un ; comme séparateur / délimiteur.
* Idéalement, passez tous vos jeux de données en UTF-8. Pour cela le programme Notepad++ fait cela très bien.
* Idéalement, exportez vos tableurs favoris (Microsoft, Libre et Open Office) au format CSV.
* Restreindre vos titres de colonnes à moins de 62 caractères.
* Ne pas doublonner le titre d'une colonne.
* En théorie les caractères spéciaux ('\:.,( -') sont acceptés, mais c'est beaucoup mieux de les éviter dans les titres.
* Harmoniser le type de vos données (et oui vos données sont typées!) : en effet si une colonne ne comporte que des chiffres, le datastore autodéterminera le type de cette colonne comme étant un nombre. Or il suffit qu'une cellule de la colonne contienne l'entrée N/A, pour que le datastore génére une erreur. 
Pour éviter les erreurs de type, il est préférable de les corriger avant d'indexer le jeu de donnée dans DataSud ou bien de transformer la valeur des cellules en cellules au format TEXTE. Cela n'est pas satisfaisant, mais ca fonctionne.

* ERREUR : En cas d'erreur supprimez complètement la ressource associée au jeu de données et ajoutez en une nouvelle.

.. Note:: **Attention avec Excel** 
* lorque le fichier contient plusieurs feuillet (ou onglet), seule la dernière feuille de calcul est indexée dans le datastore. Il est donc nécessaire de déplacer la feuille de calcul contenant les données que vous souhaitez indexer dans le datastore en dernière place de votre tableur.

* si vous ne voulez pas indexer vos données dans le datastore (pour plein de bonnes et mauvaises raisons), il suffit d'ajouter une feuille de calcul vide en dernière place de votre tableur. ::


-----------------------------------------------------
Géolocalisation des données tabulaires (XLS et CSV)
-----------------------------------------------------

Une carte peut automatiquement être générée à partir de vos données tabulaires geolocalisées. 
Pour cela vous devez intituler deux colonnes du tableau "latitude" et "longitude".

Projections : en cours de rédaction.

-------------------------------------------------------
Renseigner les métadonnées INSPIRE
-------------------------------------------------------

Cette partie de la documentation est en cours de rédaction par le CRIGE


