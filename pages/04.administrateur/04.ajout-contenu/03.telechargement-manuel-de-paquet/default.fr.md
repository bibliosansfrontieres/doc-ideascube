---
title: 'Téléchargement manuel de paquets'
---

_Cette méthode requiert des compétences dans l'administration d'un système d'exploitation Linux._

Les paquets de contenus peuvent être des regroupements de fichiers au sein d'une archive au format ZIP, des sites statics compressés ou encore des archives au format ZIM qui contiennent des version offline de wikipedia et bien d'autres ressources.

Les paquets de contenus sont donc des médias pré-sélectionnés  qui peuvent correspondre à vos besoins ou non

## Les catalogues de contenus

Tous ces paquets de contenus sont référencés dans des catalogues : [http://catalog.ideascube.org/](http://catalog.ideascube.org/)

Voici quelques catalogues fréquements utilisés

* [Kiwix](http://www.kiwix.org/fr/) : [http://catalog.ideascube.org/kiwix.yml.html](http://catalog.ideascube.org/kiwix.yml.html)
* Sites statics : [http://catalog.ideascube.org/static-sites.yml.html](http://catalog.ideascube.org/static-sites.yml.html)
* Cartes [Open Street Map](http://openstreetmap.fr/) offline : [http://catalog.ideascube.org/osmaps.yml.html](http://catalog.ideascube.org/osmaps.yml.html)
* [Bibliothèques sans frontières](http://bibliosansfrontieres.org/) : [http://catalog.ideascube.org/omeka.yml.html](http://catalog.ideascube.org/omeka.yml.html)

Tout ces catalogues sont ajoutés automatiquement sur les serveur IdeasBox et les KoomBook, cependant vous pouvez vérifier leurs présences

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog remotes list
IDEASCUBE_ID=idb
Importing settings from ideascube.conf.idb

          [Kiwix] Kiwix ZIM content : http://catalog.ideascube.org/kiwix.yml
 [OSMybon] Experimental OSM catalog : http://catalog.ideascube.org/osmaps.yml
             [Omeka] Omeka packages : http://catalog.ideascube.org/omeka.yml
         [StaticSites] Static sites : http://catalog.ideascube.org/static-sites.yml
 [bibliotecamovil] Spanish packages : http://catalog.ideascube.org/bibliotecamovil.yml
```

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog remotes -h
```

L''argument **-h **vous permet d'afficher la liste des actions disponibles  pour la gestion des catalogues \(ajout, suppression, liste\)

## Listing des contenus disponibles
### Mise à jour du catalogue
```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog cache update
```

Pour lister l'ensemble des contenus disponible dans ces catalogues, vous pouvez lancer la commande suivante

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog list
```

Activer la pagination avec l'option** **`more`

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog list | more
```

Chaque paquet est présenté de la sorte :

| Nom du paquet | Version \(date\) | Taille | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| apprenez-le-francais-niveau-a1-fr | 2017-10-27 | 549.0 MB | zipped-medias | Apprenez le français - Niveau A1 |
| wikipedia.sw | 2017-01-09 | 498.7 MB | zipped-zim | Wikipedia |

## Installation d'un paquet de contenu

### Mise à jour du catalogue
```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog cache update
```

### Installation des nouveaux paquets

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog install apprenez-le-francais-niveau-a1-fr wikipedia.sw
```

La commande ideascube à l'avantage de pouvoir prendre autant de noms de paquets que vous souhaitez en argument, chaque paquet doit être séparé par un **espace**

**INFORMATION IMPORTANTE**

* Vérifiez bien le champ `taille` et veillez à ce qu'il soit en adéquation avec votre connexion Internet. En effet, plus vous allez ajouter de contenus à télécharger et plus le traitement sera long.
* Veillez à avoir au minimum à chaque fois le double de l'espace occupé par un paquet de contenus sur votre espace de stockage
* Pour chaque paquet installé, un lien en page d'accueil sera créé, si vous souhaitez le désactiver référez vous à la [Gestion de la page d'accueil](/gestion_de_la_page_daccueil.md)

## Suppression d'un paquet

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog remove apprenez-le-francais-niveau-a1-fr
```



