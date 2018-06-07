---
title: 'Manually Download a Content Package'
---

_This option requires you to know how to use Linux._

Content packages can be file groupings within a ZIP archive, compressed static sites, or ZIM format archives.  They can contain offline versions of Wikipedia and many other resources.

Content packages are thus pre-selected media that may or may not meet your needs.

## Content Catalogues

All the content packs can be viewed in these catalogs: [http://catalog.ideascube.org/](http://catalog.ideascube.org/)

Here are some catalogues that are frequently used: 

* [Kiwix](http://www.kiwix.org/fr/) : [http://catalog.ideascube.org/kiwix.yml.html](http://catalog.ideascube.org/kiwix.yml.html)
* Static sites: [http://catalog.ideascube.org/static-sites.yml.html](http://catalog.ideascube.org/static-sites.yml.html)
* [Open Street Map](http://openstreetmap.fr/) offline : [http://catalog.ideascube.org/osmaps.yml.html](http://catalog.ideascube.org/osmaps.yml.html)
* [Libraries Without Borders](https://www.librarieswithoutborders.org/) : [http://catalog.ideascube.org/omeka.yml.html](http://catalog.ideascube.org/omeka.yml.html)

All of these catalogues are automatically added to the IdeasBox and KoomBook servers.  However, you can verify their presence: 

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
The argument **-h** allows you to view the list of actions to manage the catalogue (add, delete, list)

## Listing Available Content

To list all of the content available in the catalogues, you can run this command: 

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog list
```

Enable pagination by selecting **`more`**

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog list | more
```

Each packet is presented like this:

| Nom du paquet | Version \(date\) | Size | Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| apprenez-le-francais-niveau-a1-fr | 2017-10-27 | 549.0 MB | zipped-medias | Apprenez le français - Niveau A1 |
| wikipedia.sw | 2017-01-09 | 498.7 MB | zipped-zim | Wikipedia |

## Installing a Content Package

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog install apprenez-le-francais-niveau-a1-fr wikipedia.sw
```

The Ideascube command can accept as many packages as you would like in an argument.  Each package must be separated by a **space**.

**Important Information**

* Check the `size` of your file, and make sure the internet connection is adequate.  The more content you add, the longer it will take to download.
* Make sure you have at least twice the space necessary available in your storage space
* For each package installed, a link on the welcome page will be created.  If you want to deactivate this go to: [Gestion de la page d'accueil](/gestion_de_la_page_daccueil.md)

## Deleting a Package

```
ideascube@kb-cod-rfi-385 ~ $ ideascube catalog remove apprenez-le-francais-niveau-a1-fr
```



