.. title:: Accueil de la documentation de DATASUD

*****
Bienvenue dans la documentation de DATASUD
*****

Cette documentation est organisée en plusieurs parties, chacune correspondant à un usage particulier de la plateforme.
Le catalogue des données et des ressources disponibles sont amenés à évoluer avec la version 3 de DataSud.
La version 2 de DATASUD est disponible depuis le 15 décembre 2018.

Table des matières
==================

.. toctree::
   :titlesonly:
   :maxdepth: 0
 
   consultation
   Espace utilisateur <utilisateurs>
   contributeurs
   referents
   developpeurs

DataSud, c'est ...
==================
DATASUD est une infrastructure de données à l’échelle régionale, accessibles à travers un catalogue de données à l'échelon régional.
Elle est issue d'un projet piloté par le CRIGE Provence-Alpes-Côte d’Azur et la Région SUD Provence Alpes-Côte d’Azur, avec la participation financière de l’État et du Conseil départemental des Hautes-Alpes lancé fin 2016.

Le catalogue de données diffuse des données ouvertes, géographiques et intelligentes au service du développement des territoires et de l’innovation numérique.
80 organisations diffusent déjà des données sur DATASUD. Des données supplémentaires vont être intégrées au fil de l'eau en 2019, en particulier toutes les données du Géoportail régional du CRIGE.

Pour quel public ?
==================
DATASUD s'adresse : 
	* aux producteurs de données en région, pour référencer et diffuser leur patrimoine de données à l'échelon régional ;
	* aux réutilisateurs pour trouver des données, les croiser, les analyser afin de développer le territoire régional ;
	* aux entreprises et start-up, à la recherche de données et de services performants pour proposer les applications innovantes de demain ;
	* aux citoyens et acteurs de la transparence de l'action publique.

Quels types de données trouve-t-on dans DataSud ?
==================
DATASUD référence préférentiellement : 
	* des données ouvertes ;
	* des données intelligentes ;
	* des données géographiques.
	
	DATASUD permet également de référencer des données **sensibles**, en offrant la possiblité d'ouvrir ou non des accès à des utilisateurs ou des organisations.
	Pour favoriser les réutilisations, les données sont préférentiellement proposées dans des formats ouverts : CSV, JSON, GEOJSON, GPKG, JPEG2000, GeoTIFF.
	Elles sont ainsi lisibles dans un maximum d'applications et de logiciels.

Qui peut s'inscrire à DATASUD ?
==================

.. note::
   Toute personne, morale ou physique peut s'inscrire. L'inscription à DATASUD est gratuite et individuelle, sous réserve d'accepter les « conditions d’utilisation » de la plateforme.

Qui peut publier des données ?
==================
Toute personne, morale ou physique, publique ou privée, producteur de données publiques ou privées peut publier des données sur DATASUD, sous réserve d'accepter les « conditions d’utilisation » et de respecter la réglementation sur les données à caractères personnelles.

Plus précisément, vous pouvez publier des données sur datasud.fr :
    * si vous produisez ou collectez des données dans le cadre d’une mission de service public, à condition que ces données ne contiennent pas d’informations personnelles et qu’elles ne révèlent pas d'informations confidentielles ;
    * si vous enrichissez ou complétez des données pour le compte d’une association, d’un projet de recherche, ou sur votre temps libre ;
    * si vous produisez des données d’intérêt public, même hors du cadre d’une mission de service public ;
    * si vous produisez des données *privées* ie. accessibles uniquement à certains acteurs, sous réserve de respecter la réglementation en vigueur.


Qu'est-ce qu'une Organisation pour DATASUD ?
==================
Les organisations sont des personnes morales produisant ou intéressées par tout type de données : autorités administratives, établissements publics, associations, entreprises, start-up. Il s'agit d'entités au travers desquelles plusieurs utilisateurs peuvent collaborer sur des jeux de données.

Dans DATASUD, plusieurs contributeurs appartenant à des organisations différentes peuvent contribuer pour une organisation, moyennant validation d'un référent de ladite organisation ou d'un administrateur. Exemple : l'utilisateur 'mdupont' membre de l'organisation 'bureau d'étude' peut publier pour l'organisation 'communauté d'agglomération' car l'utilisateur 'dsi' qui est rattachée à celle-ci l'y a préalablement autorisé.


Quels services et fonctionnalités sont fournis par DATASUD ?
==================
DATASUD repose sur un **catalogue unique** à l'échelle régionale pour toutes les données tabulaires ou géographiques, proposant un **guichet unique et simplifiée de publication de données**. Ce catalogue sur la technologie 'CKAN <https://ckan.org/>'.

À travers ce catalogue, il permet aux **utilisateurs** de rechercher et de trouver des jeux de données, de les **télécharger en 1-clic**, de s'abonner et de déclarer des réutilisations faites avec des jeux de données de DATASUD.
Les **producteurs** ou contributeurs de données 

DATASUD propose également des outils métier pour les utilisateurs plus experts :
	* publication des données tabulaires par API : l'outil CKAN
	* publication d'API (ou flux) de données géographiques selon les standards WMS et WFS ;
	* publication de métadonnées INSPIRE : DATASUD offre aux organisations concernées la possibilité d'indexer leurs métadonnées de données géographiques selon le formalisme requis par le Directive INSPIRE ;
	* catalogage "en marque blanche" intégrable sur tout site internet ou tout portail institutionnel ; 
	* l'extraction de données raster et vecteur à travers l'extracteur de données géographiques du CRIGE ; 
	* la co-visualisation de données géographiques à travers l'outil de création de visionneuse du CRIGE ; 

.. note::
	Les deux derniers services sont accessibles uniquement aux partenaires du CRIGE.

Je dispose déjà d'un catalogue de données
==================
DATASUD offre la possibilité de "moissonner", c'est-à-dire de référencer des jeux de données publiées sur des catalogues existants. 
Pour l'instant, il offre cette possibilité pour les types de catalogues suivant :
	* CKAN 2.*
	* GeoNetwork 3.*
	* ISOGEO

Si vous êtes dans cette situation et souhaitez référencer vos jeux de données, contactez les administrateurs de Datasud via la formulaire de contact ou sur  contact@datasud.fr en indiquant votre demande.
	
Je suis développeur et souhaite utilisez les API de DATASUD
==================
Le catalogue de DataSud (https://trouver.datasud.fr) est construit à partir du système d’information OpenSource dédié à la gestion de catalogues de données 'CKAN <https://ckan.org/>'. 

L'application CKAN propose une API REST permettant d'interroger et de consulter les jeux de données et leurs ressources référencés dans le catalogue, soit selon le formalisme de CKAN soit selon le standard DCAT. Elle permet également de requêter et d'exposer directement le contenu (ou une partie du contenu) des ressources tabulaires (CSV, XLS). Vous trouverez plus de détails sur les méthodes offertes ici.

DATASUD offre en plus la possibilité de requêter et d'exposer le contenu des données géographiques selon les standards d'API WMS et WFS grâce à l'outil MapServer. Vous trouverez plus de détails sur les méthodes offertes ici.


.. seealso::

   :doc:`contents`

.. note::

   Ces guides sont maintenus par l'équipe Datasud (administrateurs de la Région SUD et du CRIGE Provence-Alpes-Côte d'Azur). 
