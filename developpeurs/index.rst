.. _action developpeurs:

-------------------------------
Espace développeurs
-------------------------------

Service API Ckan
================

Le site **https://trouver.datasud.fr** est construit sur le catalogue `CKAN <http://www.ckan.org/>`_. De fait, il propose une API permettant d'interroger et de consulter le catalogue des données et leurs ressources. L'API permet également de requêter directement le contenu des ressources tabulaires (CSV, XLS) lorsque celles-ci ont été correctement intégrées au [Datastore](http://datasud.readthedocs.io/fr/latest/producteurs.html#datastore-et-donnees-intelligentes) 


Ainsi, il est par exemple possible de réaliser ce qui suit.

* Obtenir au format JSON, la liste des jeux de données, des groupes thématiques, des mots-clés utilisés ou des organisations du catalogue :

  http://trouver.datasud.fr/api/3/action/package_list

  http://trouver.datasud.fr/api/3/action/group_list

  http://trouver.datasud.fr/api/3/action/tag_list
  
  http://trouver.datasud.fr/api/3/action/organization_list
  
* Obtenir un flux des jeux de données récemment mis à jour :

  http://trouver.datasud.fr/api/3/action/recently_changed_packages_activity_list

* Obtenir une réprésentation détaillée d'un des objets (jeu de données, organisation, ressource), toujours au format JSON :

* Obtenir une représentation détaillée d'un jeu de données :
  https://trouver.datasud.fr/api/3/action/package_show?id=arbres-proteges-a-digne-les-bains
  
* Obtenir une représentation détaillée d'une organisation : 
  https://trouver.datasud.fr/api/3/action/organization_show?id=air-paca

* Obtenir une liste de jeux de données "géographiques" :
  https://trouver.datasud.fr/api/3/action/package_list?datatype=donnees-geographiques
  
* Obtenier des informations sur la thématique "Environnement et Climat".
  https://trouver.datasud.fr/api/3/action/group_show?id=environnement-et-climat

* Rechercher de jeux de données à partir d'un mot clé :
  https://trouver.datasud.fr/api/3/action/package_search?q=energies

* Rechercher des jeux de données "géographiques", au format CSV, associés à la thématique Culture, patrimoine et tourisme :
  https://trouver.datasud.fr/api/3/action/package_search?fq=+res_format:CSV+datatype:donnees-geographiques+groups:culture-patrimoine-et-tourisme
  

DataSud.fr permet également de requêter directement les ressources des jeux de données. Comme eqpliqué plus haut, le Datastore propose un service d'indexation des données tablulaires (CSV et XLS) dans un datastore (base PostreSQL). Ce service permet d'exposer le contenu des ressources dont on peut ainsi requêter tout ou partie sans avoir à télécharger le jeu de données. 

* Afficher les cinq enregistrements du jeu de données des hôtels en région Provence-Alpes-Côte d'Azur :
* https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&limit=5 

* Trouver toutes les entreprises de la base INFOGREFFE 2017 dont le champ ville est égal à MARSEILLE::

    [https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&filters={"Ville":"MARSEILLE"}](https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&filters={"Ville":"MARSEILLE"})

Résultat : http://bit.ly/2oliZId

* Trouvez toutes les entreprises de la base INFOGREFFE 2017 de la ville de MARSEILLE avec le code APE 6831Z, et afficher les résultats à partir du centième (série de 100 à 199) ::

    https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&filters={%22Ville%22:%22MARSEILLE%22,%22Code%20APE%22:%226831Z%22}&offset=100

Résultat : http://bit.ly/2oliZId

Documentation de l'API (catalogue et ressources) et de l'API Datastore (requête sur les ressources) en anglais :

http://docs.ckan.org/en/latest/api/
http://docs.ckan.org/en/ckan-2.7.2/maintaining/datastore.html#the-datastore-api

Autres exemples de requête à l'API :
http://datasud.readthedocs.io/fr/latest/developpeurs/index.html#exemples-de-requete-a-l-api-ckan  

.. note:: le mot "package" qu'on trouve dans certaines requête correspond à un jeu de donnée.


Construire une requête pour l'API
=================================

Pour appeler l'API CKAN, postez un dictionnaire JSON dans une requête HTTP POST sur l'une des URL d'API de CKAN. Les paramètres de la fonction API doivent être indiqués dans le dictionnaire JSON. CKAN retournera également sa réponse dans un dictionnaire JSON.

Une façon de publier un dictionnaire JSON sur une URL est d'utiliser le client HTTP en ligne de commande `HTTPie <http://httpie.org/>`_. Il existe également d'autres outils comme Postman. Par exemple, pour obtenir une liste des noms de tous les jeux de données du groupe ``environnment`` sur le site, installez HTTPie, puis appelez la fonction API ``group_list`` en exécutant cette commande dans un terminal::

    http http://trouver.datasud.fr/api/3/action/group_list

La réponse de CKAN ressemblera à ceci::

    {
        "help": "...",
        "result": [
            "data-explorer",
            "department-of-ricky",
            "geo-examples",
            "geothermal-data",
            "reykjavik",
            "skeenawild-conservation-trust"
        ],
        "success": true
    }

La réponse est un dictionnaire JSON avec 3 clés :

1. ``"success"``: ``true`` or ``false``.

   L'API est conçue pour retourner à chaque fois un ``200 OK`` dans le code statut de sa réponse, qu'il y ait une erreur ou non dans la requête, il est donc important de toujours vérifier la valeur de la clé ``success`` dans le dictionnaire de réponse, et si elle est à false, de vérifier la valeur de la clé ``error``.

.. note::

    S'il y a vraiment un gros problème de syntaxe dans la requête à l'API, CKAN
    pourra retourner une réponse HTTP avec un status code ``409``, ``400`` or ``500``
    (dans l'ordre croissant de gravité). Dans les prochaines versions de CKAN, il est prévu
    d'essayer de supprimer ce type de réponse pour n'avoirà la place que des retours ``200 OK``
    et utiliser les valeurs ``"success"`` et ``"error"``.

2. ``"result"``: le résultat retournée par la fonction appelée. Le type et la valeur du résultat
   dépendent de la fonction appelée. Dans le cas de la fonction ``group_list``, il s'agit d'une liste
   de chaînes, les noms de tous les jeux de données qui appartiennent au groupe.

   Si c'est une erreur qui est retournée à la requête, le dictionnaire contiendra une clé ``"error"`` 
   avec le détail de l'erreur au lieu de la clé ``"result"``. 
   Un dictionnaire de réponse contenant une erreur ressemblera à 
   ceci::

       {
           "help": "Creates a package",
           "success": false,
           "error": {
               "message": "Access denied",
               "__type": "Authorization Error"
               }
        }

3. ``"help"``: le texte de documentation de la fonction appelée.

La même requête HTTP peut être effectuée en utilisant le module Python standard ``urllib2``
avec ce code Python ::

    #!/usr/bin/env python
    import urllib2
    import urllib
    import json
    import pprint

    # Make the HTTP request.
    response = urllib2.urlopen('http://demo.ckan.org/api/3/action/group_list',
            data_string)
    assert response.code == 200

    # Use the json module to load CKAN's response into a dictionary.
    response_dict = json.loads(response.read())

    # Check the contents of the response.
    assert response_dict['success'] is True
    result = response_dict['result']
    pprint.pprint(result)



Versions de l'API
=================
Les API CKAN sont versionnées. Si vous faites une demande à une URL d'API sans
numéro de version, CKAN choisira la dernière version de l'API::

    https://trouver.datasud.fr/api/action/package_list

Vous pouvez également spécifier le numéro de version de l'API souhaité dans l'URL
que vous envoyez::

    https://trouver.datasud.fr/api/3/action/package_list

La version 3 est actuellement la seule version de l'API Action.

Nous vous recommandons de spécifier le numéro d'API dans vos demandes, car cela
garantit que votre client API continuera à fonctionner si un jour le site est mis à niveau 
vers de nouvelles versions de CKAN). 

.. _api authentication:


Authentification et clés 
========================

Certaines fonctions de l'API nécessitent une autorisation, par exemple pour ajouter ou modifier des jeux de données et desressources). L'API utilise la même fonction d'autorisation
et la configuration en tant qu'interface web, donc si un utilisateur est autorisé à
faire quelque chose dans l'interface web, ils sera autorisés à le faire via l'API de la même façon.

Lorsque vous appelez une fonction de l'API nécessitant une autorisation, vous devez vous authentifier
vous-même en fournissant votre clé API avec votre requête HTTP. Pour trouver votre clé API, 
connectez-vous au site CKAN en utilisant son interface web et visitez votre profil utilisateur.

Pour fournir votre clé API dans une requête HTTP, incluez-la dans un En-tête `` Authorization`` ou `` X-CKAN-API-Key``.

Par exemple, pour demander si vous suivez actuellement l'utilisateur
`` markw`` sur demo.ckan.org en utilisant HTTPie, exécutez cette commande::

    https://trouver.datasud.fr/api/3/action/am_following_user id = markw Autorisation: XXX

(Remplacer `` XXX`` avec votre clé API.)

Par exemple, pour obtenir la liste des activités de votre tableau de bord utilisateur, on lance ce code Python ::
    request = urllib2.Request('http://trouver.datasud.fr/api/3/action/dashboard_activity_list')
    request.add_header('Authorization', 'XXX')
    response_dict = json.loads(urllib2.urlopen(request, '{}').read())


Support JSONP
=============


Pour répondre aux scripts d'autres sites qui souhaitent accéder à l'API, les données peuvent
être renvoyé au format JSONP, où les données JSON sont 'complétées' avec une fonction
call. La fonction est nommée dans le paramètre 'callback'. Par exemple:

https://trouver.datasud.fr/api/3/action/package_show?id=adur_district_spending&callback=myfunction

.. note :: Cela ne fonctionne qu'avec les requêtes GET


.. _api-examples:


Exemples de requête à l'API CKAN
========


Tags (mots clés, hors thésaurus)
--------------------------------

Liste de tous les tags :

* browser: https://trouver.datasud.fr/api/3/action/tag_list
* curl: ``curl https://trouver.datasud.fr/api/3/action/tag_list``
* ckanapi: ``ckanapi -r https://trouver.datasud.fr action tag_list``

Top 10 des tags utilisés dans les jeux de données :

* browser: https://trouver.datasud.fr/api/action/package_search?facet.field=[%22tags%22]&facet.limit=10&rows=0
* curl: ``curl 'https://trouver.datasud.fr/api/action/package_search?facet.field=\["tags"\]&facet.limit=10&rows=0'``
* ckanapi: ``ckanapi -r https://trouver.datasud.fr action package_search facet.field='["tags"]' facet.limit=10 rows=0``

Autres exemples de requêtes basées sur la même logique de construction :

* Tous les jeux de données
* http://trouver.datasud.fr/api/3/action/package_list


* Toutes les thématiques 
* http://trouver.datasud.fr/api/3/action/group_list


* Tous les mots clés
* http://trouver.datasud.fr/api/3/action/tag_list


* Toutes les organisations
* http://trouver.datasud.fr/api/3/action/organization_list


* Obtenir un flux des jeux de données récemment mis à jour :
* http://trouver.datasud.fr/api/3/action/recently_changed_packages_activity_list

**Obtenir une représentation détaillée d'un des objets (jeu de données, organisation, ressource), toujours au format JSON :**

*  Obtenir une représentation détaillée d'un jeu de données :
*  https://trouver.datasud.fr/api/3/action/package_show?id=arbres-proteges-a-digne-les-bains


*  Obtenir une réprésentation détaillée d'une organisation :
* https://trouver.datasud.fr/api/3/action/organization_show?id=region-sud

**Autres exemples :**

*  Obtenir une liste de jeux de données "géographiques" :
*  https://trouver.datasud.fr/api/3/action/package_list?datatype=donnees-geographiques


*  Obtenier des informations sur la thématique "Environnement et Climat".
*  https://trouver.datasud.fr/api/3/action/group_show?id=environnement-et-climat


*  Rechercher des jeux de données à partir d'une requête textuelle :
*  https://trouver.datasud.fr/api/3/action/package_search?q=energies


*  Rechercher des jeux de données "géographiques", au format CSV, associé à la thématique Culture, patrimoine et tourisme :
*  https://trouver.datasud.fr/api/3/action/package_search?fq=+res_format:CSV+datatype:donnees-geographiques+groups:culture-patrimoine-et-tourisme

* sur la donnée indexée dans le Datastore :
* Trouvez toutes les entreprises de la base INFOGREFFE 2017 dont le champ ville est égal à MARSEILLE::

    [https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&filters={"Ville":"MARSEILLE"}](https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&filters={"Ville":"MARSEILLE"})

Résultat : http://bit.ly/2BKn6VW

* Trouvez toutes les entreprises de la base INFOGREFFE 2017 de la ville de MARSEILLE avec le code APE 6831Z, et afficher les résultats à partir du centième (série de 100 à 199) ::

    https://trouver.datasud.fr/api/3/action/datastore_search?resource_id=9723b8ba-8379-4b1f-a85c-1f0efe916ce8&filters={%22Ville%22:%22MARSEILLE%22,%22Code%20APE%22:%226831Z%22}&offset=100

Résultat : http://bit.ly/2oliZId





Service WMS
===========

En cours.


Service WFS
===========

En cours.

Service CSW
===========

En cours.
