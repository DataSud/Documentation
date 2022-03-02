====================
Espace contributeurs
====================


Ce guide est destiné aux producteurs de données, déjà inscrit en tant qu'Utilisateurs https://publier.datasud.fr/ et souhaitant contribuer à l'enrichissement des publications sur la plateforme.
`« voir la documentation sur les Utilisateurs » <https://datasud.readthedocs.io/fr/latest/utilisateurs.html/>`_ 

.. note:: Toute personne, morale ou physique, publique ou privée, producteur de données publiques ou privées peut les publier sur la DataSud, sous reserve d'accepter les « conditions d’utilisation » et de respecter la réglementation sur les données à caractères personnelles.

--------------------------------------------------------
Devenir Contributeur et Référent pour une organisation
--------------------------------------------------------

Les organisations sont le plus souvent des personnes morales (autorités administratives, associations, entreprises) ou également des groupes informels.

.. note:: **La création d'une nouvelle organisation peut-être effectuée soit au moment de votre inscription comme utilisateur de DataSud, soit après la validation de votre profil Utilisateur par les Administrateurs de DataSud. Les demandes de statut de Contributeur ou de Référent sont soumises à la validation des Administrateurs. Il faut donc patienter un peu!** 

.. image:: DataSudFirstConnect.PNG

.. image:: DemandeOrga.PNG


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

-----------------------
Créer une Organisation
-----------------------

Toute demande de création d'une organisation est soumise à l'administrateur du site pour validation

.. image:: DataSudAjoutOrga.PNG

La dénomination sociale est obligatoire

.. image:: Creation_orga1.PNG

La description est facultative mais fortement conseillée, d'une part pour permettre de qualifier l'Organisation et sa démarche en matière d'ouverture des données publiques et géographiques et d'autre part pour permettre l'implementation automatique d'une page web spécifique à propos de l'organisation.

.. image:: Creation_orga2.PNG


-----------------------------------
Editer la page d'une Organisation
-----------------------------------


Pour éditer la page de son organisation, le Contributeur clique sur l'onglet ORGANISATIONS dans son espace d'administration. 

.. image:: Onglet_organisation.PNG

La première fois que le contributeur édite la page de son organisation, il lui sera demandé de définir le territoire de compétence de l'organisation. La création de ce territoire de compétences permet de bénéficier de fonctionnalités spatiales supplémentaires dans DataSud.

.. image:: Territoire_competence.PNG


------------------------------------------------------------------------
Tableau de bord des datasets et ressources publiées (publier.datasud.fr)
------------------------------------------------------------------------

Depuis l'onglet "Jeux de données", tous les utilisateurs inscrits accèdent à un dashboard des datasets qu'ils publient.

* Le sous-onglet « Mes jeux de données » présente les datasets publiés par l’utilisateur, toutes organisations confondues.
* Le sous-onglet « Tous les jeux de données » présente à l'utilisateur tous les jeux de données qu'il a publié ainsi que tous les jeux de données publiés pour les organisations dont il est le référent.
* Les trois sous-onglets suivants "Jeux de données moissonnés CKAN", "Jeux de données moissonnés CSW" et "Jeux de données moissonnés DCAT" présente à l'utilisateur les jeux de données issus de moissonnages de catalogues distants.

.. image:: publier_donnees.PNG

En sélectionnant un jeu de données, l'utilisateur peut :

* le supprimer,
* éditer le jeu de données, les ressources associées ou la fiche de métadonnées Inspire,
* ouvrir le dataset dans le catalogue CKAN.

.. image:: Dataset_boutons_bas.png

-------------------------
Publier un jeu de données 
-------------------------

* Pour publier un jeu de donner le Contributeur se connecte avec son identifiant et mot de passe sur https://publier.datasud.fr

.. image:: InscriptionDataSud.PNG

**La publication se fait en deux étapes successives:** 

Tout d'abord on renseigne les métadonnées servant à définir ou décrire le jeu de données qui sera publié, puis on ajoute des jeux de données brutes ou des ressources complémentaires.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Etape n°1 : Renseigner les métadonnées
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: Edit_newdataset1.PNG

.. note:: De nombreux mots-clés sont déjà répertoriés dans la base. Ils apparaissent dans une liste déroulante lorsque vous saisissez les premières lettres du mot. Mieux vaut choisir un mot clés existant, plutot que d'en choisir un nouveau afin de permettre de relier votre jeu de donnée à d'autres jeux similaires inscrits au catalogue de DataSud.

.. image:: Edit_newdataset2.PNG

.. image:: Edit_newdataset3.PNG

**Les métadonnées obligatoires sont les suivantes :**

- Titre
- Organisation à laquelle est rattaché ce jeu de données
- Descriptif  : C'est un champ incontournable pour garantir une bonne réutilisation, car une donnée bien décrite est une donnée bien réutilisée !
- Dates de création, de dernière modification et de publication : la valeur par défaut indique la date du jour et la date de modification se met à jour automatiquement lorsque vous enregistrez des modifications sur les ressources.
- Licence : Selectionner une licence parmi celles qui sont proposées: Creative Commons attribution 4.0; Licence ouverte V2.0; Creative Commons cc-by-nc-nd 3.0, Open data base Licence V1.0 ou une Licence Spécifique.



**Les métadonnées facultatives sont les suivantes :**

- Illustration : le nom de l'image que vous souhaitez mettre en illustration du jeu de donnée ne doit pas contenir d'accent. le format de l'illustration peut-être du .Jpg ou .png;
- Catégories : sélectionnez dans la liste une ou plusieurs thématiques proposées correspondant à la/ les catégories associées au jeu de donnée;
- Mots-clés : privilégiez les mots clés écrits au singulier et en minuscule;
- Fréquence de mise à jour : à choisir dans la liste déroulante "Lorsque nécessaire" ; "Non planifiée"; "Irrégulière"; "Continue"; "Temps réel"; "Journalière"; "Hebdomadaire"; "Bi-mensuelle"; "Mensuelle"; "Trimestrielle"; "Bi-annuelle"; "Annuelle"; "Inconnue".
- Type de données : Données ouvertes ( correspond aux données statistiques ou tout autre jeu de donnée ne contenant pas de composante géographique; Données intelligentes ( voir le passage ci dessous au sujet du  `« Datastore » <https://datasud.readthedocs.io/fr/latest/contributeurs.html#datastore-et-donnees-intelligentes>`_   ; Données géographiques ( avec des cooordonnées géographique de géolocalisation ) 
- Meta-données INSPIRE
- Fréquence de mise à jour
- Couverture régionale


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Etape n°2 : Publier une ressource
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il existe quatre manières différentes d'ajouter un jeu de données :

**1.	Téléverser manuellement un fichier depuis votre poste local:** 

A l'aide du bouton Parcourir, vous pouvez déposer le fichier qui s’ajoute dans l’entrepôt de données DataSud;
 
.. image:: Upload_ressources.PNG

Le **Titre** de votre fichier est automatiquement recopié, mais il est possible de modifier manuellement le nommage de ce jeu de donnée.

.. image:: Upload_ressources1.PNG


Le format du fichier est automatiquement reconnu par DataSud.
il faut préciser si le jeu de donnée est disponible en tant que Données brutes ou si c'est une documentation associée au jeu de donnée pour permettre aux visiteurs de DataSud d'avoir des informations complémentaires ( plaquettes de communications, affiches, photographie, site internet....)

**2.	Télécharger un jeu de donnée depuis une URL de téléchargement :**

Dans ce cas, Datasud va télécharger la ressource pour l'ajouter dans l’entrepôt de données; 

.. image:: Upload_ressources_URL.PNG

Ce mode de publication permet de synchroniser la ressource distante, selon une périodicité régulière à indiquer : 

* Jamais
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

Dans ce cas, la ressource n'est pas téléchargée dans DataSud et vous indiquez précisement l'adresse URL de téléchargement de la donnée qui reste hebergée chez son producteur. 
Cette donnée apparait au catalogue de DataSud mais elle n'est pas hébergée dans son entrepot.

.. image:: Upload_ressources_ref_URL.PNG

**4.	Dépot sFTP:**

Le programme sftp apporte une interface similaire au programme ftp qui permet de publier des fichiers à distance. 
Pour vous connecter à votre dépôt Sftp et déposer un fichier vous pouvez le faire avec un logiciel SSH, en voici quelques-uns :

* Filezilla (The free FTP solution https://filezilla-project.org/)
* Putty ( 0.75 pour Windows - Télécharger sur https://putty.fr.uptodown.com/windows
*	mobaXterm (MobaXterm free Xserver and tabbed SSH client for Windows sur https://mobaxterm.mobatek.net/)


.. image:: DepotsFTP.JPG

Paramètre de connexion : 

* L'adresse de connexion est : sftp://sftp.datasud.fr
* Le port est le : 921
* Les utilisateurs doivent utiliser leur login/mdp de DataSud pour se connecter et accéder à leur espace
* Une fois connecté, vous avez accès à votre espace de dépôt sFTP et vous pouvez y déposer des fichiers, 
* puis vous pouvez déposer directement sur DataSud les jeux de données depuis votre espace sFTP

.. note:: Il peut arriver que la connexion au serveur SFTP ne fonctionne pas lorsque le Proxy de votre organisation bloque l'accès au compte SFTP; Veuillez pour cela tester la connexion à partir d'un autre point d'accès internet sans Proxy ( depuis un smartphone ou une connexion internet personnelle).

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Restriction d'accès des ressources
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il est possible de restreindre l’accès des ressources publiées. Dès qu'une modification est enregistrée sur la ressource concernée, une notification est envoyée aux utilisateurs pour lesquels l'accès est accordé. 

Le contributeur peut choisir plusieurs types de restrictions :

* à un ou plusieurs organismes (à choisir dans une liste déroulante) : dans ce cas seuls les utilisateurs rattachés à ces organismes pourront accéder à la ressource.
* à une liste d’utilisateur inscrits sur la plateforme (à choisir dans une liste déroulante).
* à tous les utilisateurs possédant un compte.
* à tous les utilisateurs « partenaires ».

.. note:: Le mail renseigné dans le champ "Email du diffuseur" est utilisé pour la réception des demandes d'accès aux données sécurisées. Aussi, les contributeurs peuvent indiquer une adresse mail particulière pour être informés de ces demandes d'accès.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Publication en mode privé d'un jeu de données
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il est possible de publier un jeu de données en mode « Privé » : dans ce cas, seuls les administrateurs de la plateforme ainsi que les utilisateurs rattachés à l’organisation qui publie pourront accéder au jeu de données dans le catalogue CKAN.
Ce mode de publication peut être considéré comme un mode brouillon et permet de vérifier et valider sa publication dans le catalogue.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Mettre à jour un jeu de données ou une ressource
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Les données publiées peuvent être mises à jour après leur publication, que la modification porte sur un jeu données dans son ensemble, ou sur l’une des ressources qu’il contient  (Données brutes ou ressources associées).

L'actualisation d’une ressource existante permet d’en mettre à jour le contenu sans changer l’emplacement qui lui est assigné, c’est-à-dire son lien hypertexte (aussi appelé URL). Le fait d’actualiser une ressource (plutôt que de la supprimer et d'en créer ensuite une nouvelle) permet de conserver l’historique des téléchargements de cette ressource. Cela évite aussi de créer des liens rompus sur Internet, qui meneront à une erreur HTTP 404, vu que la page web n'existera plus et sera introuvable par le serveur.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Supprimer un ensemble de donnée et / ou une ressource
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Aller sur le site https://publier.datasud.fr/ et rechercher vos jeux de données; 

Il est possible de supprimer un ensemble de données ( Dataset ) comprenant les metadonnées; ou seulement les ressources et fichiers brutes associés à un ensemble de données.
Pour cela selectionner l'ensemble de données que vous souhaitez supprimer 

.. image:: Supr_Dataset.PNG

Pour confirmer, veuillez réécrire le nom du jeu de données à supprimer.

.. image:: Supr_Dataset_confirm.PNG

Il est recomandé de Copier le titre de l'ensemble de donnée ( Ctrl C) afin de conserver la même orthographe, puis coller ce titre dans la fenêtre qui s'affichera pour confirmer la suppression.

Attention, cette action est irreversible et supprimera définitivement le jeu de données ainsi que toutes les ressources qui lui sont attachées.

------------------------------------
Principe du moissonnage dans Datasud
------------------------------------

Le moissonnage permet de référencer sur DataSud des jeux de donnés provenant d'autres plateformes de données ouvertes. 
Les liens de téléchargement exposés par les catalogues d'origine sont utilisés pour créer des ressources référencées dans DataSud

Les métadonnées des ensembles de données et des ressources peuvent être issues du catalogue d'origine ou générée par DataSud au moment du moissonnage.

✴ Quel type de moissonnage de catalogue distant ?

• CSW : pour le moissonnage de catalogues exposant leurs informations selon le standard OGC (ex : Geonetwork),
• CKAN : pour le moissonnage de catalogues opendata CKAN,
• DCAT : pour le moissonnage de catalogues exposés selon le standard DCAT-AP-CH au format RDF ou Json (ex :Opendatasoft)

---------------------------------------------------------------
Valoriser un ensemble de donnée en déclarant leur réutilisation 
---------------------------------------------------------------

.. image:: Valoriser_donnees.PNG

.. image:: Ajouter_reutilisation.PNG


-----------------------------------------------------
Géolocalisation des données tabulaires (XLS et CSV)
-----------------------------------------------------

Une carte peut-être automatiquement générée à partir de vos données tabulaires geolocalisées. 
Pour cela vous devez avoir deux colonnes contenant des coordonnées géographiques ou bien une colonne géométrique (GeoJSON).

La projection utilisée est le WGS84 (EPSG : 4326).

Dans l'onglet "Grille", vous pouvez visualiser la table attributaire de vos données et vérifier qu'elles s'affichent correctement.

.. image:: csv1.PNG

Dans l'onglet "Carte", vous pouvez visualiser vos données géolocalisées et accéder aux paramètres. 

Vous pouvez choisir quel type de coordonnées vous souhaitez utiliser entre 2 attributs de type "latitude" et "longitude" ou un seul attribut de type géométrie GeoJSON. Selon votre choix, vous allez pouvoir définir la ou les colonnes qui contiennent les informations de géolocalisation. 

L'option "Marqueurs de regroupement" vous permet de "fusionner" visuellement les données proches.

.. image:: csv2.PNG

Vous pouvez également relayer cette carte sur votre site Internet en cliquant sur le bouton "Embarquer sur votre site". Il ne vous reste alors qu'à définir la taille de votre fenêtre en pixel et de copier le code sur votre site.

.. image:: csv3.PNG

Projections : en cours de rédaction.

-----------------------------------
Renseigner les métadonnées INSPIRE
-----------------------------------

Les utilisateurs qui le souhaitent peuvent associer une fiche de métadonnée Inspire au dataset.
Depuis l’interface d’édition du dataset, en cliquant sur « Editer la fiche de métadonnées INSPIRE » un formulaire présentant les nombreux champs requis pour ces fiches de métadonnées permet à l’utilisateur de créer une fiche dans Géonetwork.

Lors du premier enregistrement, les champs communs avec ceux du dataset sont pré-remplis et une fiche est créée dans Geonetwork. 

Par la suite, les modifications depuis ce formulaire sont reportées dans la fiche Geonetwork ainsi que dans le dataset IDGO.
