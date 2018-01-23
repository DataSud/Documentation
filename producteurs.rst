==================
Espace producteurs
==================

Ce guide est à destination des producteurs de données sur DataSud : http://publier-rec.datasud.fr 

---------------------------------
S'inscrire et publier sur DataSud
---------------------------------

.. note:: Toute personne, morale ou physique, publique ou privée, peut contribuer à la Plateforme, en publiant des jeux de données,  des textes, des ressources et des commentaires.


---------------------------------
Devenir Utilisateur
---------------------------------

- L’Utilisateur s’inscrit sur la Plateforme: https://publier-rec.datasud.fr
- Cette inscription est propre à sa personne et non à l’entité ou personne morale qu’il représente. 
- En s’inscrivant, l’Utilisateur crée un profil sur la Plateforme.
- En s'inscrivant, l'Utilisateur accepte les `« conditions d’utilisation » <https://www-rec.datasud.fr/conditions-dutilisation-cgus/>`_
- *Le nom d'utilisateur doit contenir uniquement des caractères alphanumériques en minuscules (ascii) et ces symboles : -_*
- l'Utilisateur doit ensuite valider votre inscription en cliquant sur le lien reçu par mail.

.. image:: CaptureDataSudConnect.PNG

.. image:: CaptureDataSudSubscribe.PNG



.. note:: L’Utilisateur dispose des fonctionnalités suivantes ::


- créer ou rejoindre une Organisation, et en devenir Membre (voir rubrique dédiée),
- accéder aux données et services autorisés pour cette Organisation,
- accéder aux données et services autorisées pour les Utilisateurs inscrits,
- demander à devenir Contributeur d’une Organisation,
- suivre/s’abonner à un Jeu de données ou une Organisation ; le partage et l’intégration d’un Jeu de données ou d’une ressource directement sur un autre site.
- participer au contrôle de la qualité de la Plateforme en signalant les contenus n’ayant pas vocation à y figurer (illicites ou contraires aux CGU).
- contacter directement le Contributeur ayant publié un Jeu de données.
- contacter les Administrateurs de la Plateforme.

.. image:: CaptureDataSudFirstConnect.PNG

---------------------------------
Devenir Contributeur
---------------------------------

Les Utilisateurs peuvent créer ou rejoindre des Organisations. Il s’agit le plus souvent de personnes morales (autorités administratives, associations, entreprises) mais également de groupes informels.

Toute personne inscrite sur la plateforme en tant qu’Utilisateur peut demander et obtenir le statut de Contributeur pour une organisation existante ou une nouvelle organisation. 

.. note:: Le Contributeur dispose des fonctionnalités suivantes :


- publier un Jeu de données et y ajouter des Ressources, sous la forme d’un fichier téléchargeable, d’un lien ou d’une API,
- autoriser l’accès aux Ressources d’un Jeu de Données dont il est Contributeur à tous les Utilisateurs inscrits, à un Utilisateur, une Organisation ou uniquement l’Organisation propriétaire du Jeu de données.

.. note:: A noter ::

- La demande de **création d'une nouvelle organisation doit se faire au moment de l'inscription**.
- La demande de statut de Contributeur peut se faire au moment de l'inscription pour une nouvelle organisation ou après l'inscription sur une organisation existante.
- Pour retrouver ses organisations le Contributeur doit cliquer sur l'onglet *mes organisations* dans son espace d'administration. 
- Les demandes de statut sont soumis à la validation des Administrateurs *à priori*. Il faut donc patientier un peu. 

.. image:: CaptureDataSudAddOrganization.PNG

*Les Administrateurs de la Plateforme se réservent la possibilité de révoquer une inscription, un statut de Contributeur ou de Référent, sans avis préalable.*

---------------------------------
Devenir Référent
---------------------------------

Toute personne inscrite sur la plateforme en tant qu’Utilisateur peut demander et obtenir le statut de Référent pour une organisation.

.. note:: Le Référent dispose des fonctionnalités suivantes ::

- éditer ou supprimer un Jeu de Données publié par un Contributeur de l’Organisation dont il est Référent
- éditer ou supprimer un statut de Membre ou de Contributeur d’un Utilisateur d’une Organisation à laquelle il appartient

.. note:: A noter ::

- La demande de statut de Référent peut se faire au moment de l'inscription pour une nouvelle organisation ou après l'inscription sur une organisation existante.
- Pour retrouver ses organisations le Contributeur doit cliquer sur l'onglet *mes organisations* dans son espace d'administration. 
- Les demandes de statut sont soumis à la validation des Administrateurs *à priori*. Il faut donc patientier un peu. 

*Les Administrateurs de la Plateforme se réservent la possibilité de révoquer une inscription, un statut de Contributeur ou de Référent, sans avis préalable.*

.. image:: CaptureDataSudAddOrganizationStatus.PNG


- *>> Catalogue de données DataSud* https://trouver-rec.datasud.fr/dataset

- *>> Liste des contributeurs DataSud* https://trouver-rec.datasud.fr/organization

- *>> Liste des thématiques DataSud* https://trouver-rec.datasud.fr/group


----------------------------------------------
Renseigner les métadonnées
----------------------------------------------

Une fois connecté à l'espace d'administration le Contributeur et le Référent peuvent ajouter des Jeux de données à leurs Organisations.


.. image:: CaptureDataSudAddDataset.PNG


.. note:: Les meta-données obligatoires sont les suivantes ::

- Titre
- Organisation
- Licence
- Dates (par défaut)

.. note:: Les meta-données facultatives sont les suivantes ::

- Descriptif
- Thématiques
- Mots-clés
- Type de données
- Meta-données INSPIRE
- Fréquence de mise à jour
- Couverture régionale

Voici quelques exemples de syntaxe Markdown. Quelques balises HTML équivalentes sont données.

Cette liste n'est pas exhaustive.

=== Formatage ===
Pour mettre du texte en emphase (balise HTML <em>), ce qui produit une mise en italique dans un navigateur courant :

 *quelques mots*

Pour mettre du texte en grande emphase (balise HTML <nowiki><strong></nowiki>), ce qui produit une mise en gras dans un navigateur courant :

 **plus important**

Pour souligner :

 __également important__

Pour mettre du code dans le texte (balise HTML <nowiki><code></nowiki>) :
 Mon texte `code` fin de mon texte

Pour un paragraphe de code, mettre quatre espaces devant :
     Première ligne de code
     Deuxième ligne

Comme dans les courriels, il est possible de faire des citations :
 > Ce texte apparaîtra dans un élément HTML <nowiki><blockquote></nowiki>.

Pour faire un nouveau paragraphe, sauter une ligne
 Premier paragraphe
 
 Deuxième paragraphe   

Pour faire un simple retour à la ligne, mettre deux espaces en fin de ligne (balise HTML <nowiki><br></nowiki>).

=== Listes ===
Sauter une ligne avant le début de la liste.

Pour créer une liste non ordonnée (balise HTML <nowiki><ul></nowiki>) :
 * Pommes
 * Poires
     * Sous élément avec au moins quatre espaces devant.
     
Et une liste ordonnée (balise HTML <nowiki><ol></nowiki>) :
 1. mon premier
 2. mon deuxième
Et une liste en mode case à cocher
 - [ ] Case non cochée
 - [x] Case cochée

=== Titres ===
Les titres sont créés avec un certain nombre de [[Croisillon (signe)|#]] avant le titre, qui correspondent au niveau de titre souhaité (le [[HTML]] propose 6 niveaux de titres de <nowiki><h1></nowiki> à <nowiki><h6></nowiki>)

 # un titre de premier niveau
 #### un titre de quatrième niveau

Pour les deux premiers niveaux de titre (<nowiki><h1></nowiki> et <nowiki><h2></nowiki>), il est également possible de souligner le titre avec des [[=]] ou des [[Tiret|-]] (leur nombre réel importe peu, mais il doit être supérieur à 2).

 Titre de niveau 1
 <nowiki>=====================</nowiki>

 Titre de niveau 2
 -------------------
=== Tableaux ===
Pour créer des tableaux (balises HTML <nowiki><tr></nowiki> et <nowiki><th>)</nowiki>
 | Titre 1       |     Titre 2     |   Titre 3      |
 | ------------- | -------------   | ---------      |
 | Colonne       |     Colonne     |      Colonne   |
 | Alignée à     |      Alignée au |     Alignée à  |
 | Gauche        |      Centre     |      Droite    |

=== Liens ===

Pour créer des liens (balise HTML <nowiki><a></nowiki>) :
 [texte du lien](url_du_lien "texte pour le titre, facultatif")

=== Images ===
Pour afficher une image (balise HTML <nowiki><img></nowiki>) :
 ![Texte alternatif](url_de_l'image "texte pour le titre, facultatif")
 

-------------------------------------------------------
Renseigner les métadonnées INSPIRE
-------------------------------------------------------

Texte...

-------------------------------------------------------
Conseils utiles
-------------------------------------------------------

- Les champs descriptifs long d'une organisation, d'un jeu de donnée et d'une ressource peuvent être mis en forme. Pour cela il faut utiliser le langage du markdown (https://fr.wikipedia.org/wiki/Markdown) plutôt que du HTML
