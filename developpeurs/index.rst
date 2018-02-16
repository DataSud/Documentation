.. _action developpeurs:

-------------------------------
Espace développeurs
-------------------------------

Service API Ckan
================

Le site **https://trouver.datasud.fr** est construit sur le catalogue `CKAN <http://www.ckan.org/>`_. De fait, il dispose d'une API permettant d'interroger et de consulter les données qu'il contient.

Ainsi, il est par exemple possible de réaliser ce qui suit.

* Obtenir au format JSON, des listes des jeux de données, des groupes thématiques ou encore des mots-clés utilisés dans le catalogue :

  http://trouver.datasud.fr/api/3/action/package_list

  http://trouver.datasud.fr/api/3/action/group_list

  http://trouver.datasud.fr/api/3/action/tag_list

* Obtenir une réprésentation d'un des objets, toujours au format JSON :

  https://trouver.datasud.fr/api/3/action/package_show?id=xxx

  https://trouver.datasud.fr/api/3/action/tag_show?id=gold

  https://trouver.datasud.fr/api/3/action/group_show?id=environnement

* Rechercher de jeux de données ou des ressources correspondants à une requête :

  https://trouver.datasud.fr/api/3/action/package_search?q=insee

  https://trouver.datasud.fr/api/3/action/resource_search?query=name:District%20Names


* Obtenir un flux des jeux de données récemment mis à jour :

  http://trouver.datasud.fr/api/3/action/recently_changed_packages_activity_list


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

Certaines fonctions de l'API nécessitent une autorisation. L'API utilise la même fonction d'autorisation
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



Fonctions de type GET
=====================

Les fonctions de l'API de type GET peuvent également être appelées avec une requête HTTP GET
Par exemple, pour obtenir la liste des jeux de données (packages) à partir de
trouver.datasud.fr, ouvrez cette URL dans votre navigateur:

https://trouver.datasud.fr/api/3/action/package_list

Ou, pour rechercher des jeux de données correspondant à la requête de recherche ``spending``,
sur trouver.datasud.fr, ouvrez cette URL dans votre navigateur:

https://trouver.datasud.fr/api/3/action/package_search?q=spending

.. note:: Les plugins de navigateur comme `JSONView pour Firefox <https://addons.mozilla.org/en-us/firefox/addon/jsonview/>` 
  ou `Chrome <https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc>`
  formatera et colorera la réponse JSON de CKAN dans votre navigateur.

La requête de recherche est envoyée en utilisant dans l'URL le paramètre ``?q=spending``. Plusieurs
paramètres peuvent être ajoutés dans l'URL, séparés par des caractères ``&``, par exemple
pour obtenir uniquement les 10 premiers jeux de données correspondants, ouvrez cette URL:

https://trouver.datasud.fr/api/3/action/package_search?q=spending&rows=10

Lorsqu'une action nécessite une liste de chaînes comme valeur d'un paramètre, la
valeur peut être envoyée en mettant plusieurs fois le paramètre dans l'URL:

https://trouver.datasud.fr/api/3/action/term_translation_show?terms=russian&terms=romantic%20novel



Support JSONP
=============

To cater for scripts from other sites that wish to access the API, the data can
be returned in JSONP format, where the JSON data is 'padded' with a function
call. The function is named in the 'callback' parameter. For example:


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

Tous les jeux de données ayant le tag 'economie':

* browser: https://trouver.datasud.fr/api/3/action/package_search?fq=tags:economie
* curl: ``curl 'https://trouver.datasud.fr/api/3/action/package_search?fq=tags:economie'``
* ckanapi: ``ckanapi -r https://trouver.datasud.fr action package_search fq='tags:economie'``


Service WMS
===========



Service WFS
===========



Service CSW
===========
