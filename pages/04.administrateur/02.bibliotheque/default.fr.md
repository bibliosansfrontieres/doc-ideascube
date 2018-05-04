---
title: 'La bibliothèque'
---

Les administrateurs ont la possibilité de créer modifier ou supprimer des livres et d'ajouter des exemplaires pour chacun des livres créés. 

## Livre et exemplaire

Pour utiliser l'application bibliothèque, il convient de saisir  la différence entre un livre et un exemplaire. Le livre est équivalent au concept, l'exemplaire à l'objet. Un livres peut se voir associer un ou plusieurs exemplaires. Il est en effet tout à fait possible d'avoir plus d'un exemplaire d'un livre dans une bibliothèque. Si aucun exemplaire n'a été créé pour un livre donné, alors celui-ci n'apparaîtra pas dans la bibliothèque.

## Création de livres

Il convient de créer d'abord un livre avant de créer un exemplaire. Pour ce faire dans l'application Bibliothèque, cliquez sur le bouton créer un livre. A noter : ce bouton n'apparaît que lorsque vous êtes connecté comme administrateur.

Le livre est donc une fiche descriptive comprenant le titre, l'auteur, le n°ISBN, une image de couverture, la série, une description, un sous-titre, une maison d'édition, une section (adulte, jeunesse, théâtre, roman, etc.), une langue, des tags.

![](bibliotheque-exemplaire.png)

## Création d'exemplaire

Une fois le livre créé, vous pouvez lui assigner un ou plusieurs exempalires. Pour ce faire, cliquer sur un livre, et cliquez sur le bouton "Ajouter un exemplaire". *A noter : ce bouton n'apparaît que lorsque vous êtes connecté en tant qu'administrateur.*

Un exemplaire est caractérisé par un code barre, des commentaires (pour indiquer l'état de l'exemplaire livre ou tout autre information utile) un emplacement s'il s'agit d'un livre papier, un fichier à uploader s'il s'agit d'un livre numérique.

![](bibliotheque-exemplaire.png)

## Prêt de livres

La création d'un exemplaire et le fait de rensiegner le code barre associé à un livre vous offre la possibilité de gérer des prêts de livres dans l'application [Prêt](lien).

## Import de livres

Il est possible d'importer plusieurs livres en une seule fois dans la bibliothèquegrâce  à l'option "importer des notices". Vous pouvez importer 4 types de ficheirs catalogues : 

* un catalogue d'une autre Ideas Box ou KoomBook au format Ideascube
* un import à partir des numéros ISBN des livres
* des fichier csv issus de [Moccam en ligne](http://www.moccam-en-ligne.fr/)
* un catalogue au format unimarc

Nous recommandons les deux premières options : un import depuis un catalogue au format ideascube ou un import  à partir des numéros ISBN.

Pour importer depuis un catalogue au format ideascube. Sélectionnez l'option "zip ideascube", cliquez sur parcourir pour sélectionner le fichier zip puis cliquez sur "Charger des notices depuis un fichier". Cette option n'est utile que si vous souhaitez importer un catalogue depuis un autre logiciel ideascube. Il faut en effet au préalable avoir fait un export depuis ideascube. Celui-ci s'effectue grâce à l'option "exporter un catalogue". L'export se fait sous forme de fichier zip. 

Pour importer des livres depuis leur numéro ISBN, saisissez les fichiers dans le champs de formulaire "Depuis ISBN". cette option ne fonctionne qu'avec une connexion Internet puisque les informations sont récupérées depuis le site http://openlibrary.org/. Nous recommandons chaleureusement aux utilisateurs d'Ideascube de renseigner les notices de livres qui ne seraient pas disponibles directement sur http://openlibrary.org/ puis de relancer l'import. Ce faisant, ces nouvelles notices bénéficieront  à toue la communauté des utilisateurs d'Ideascube et à la communauté d'openlibrary.org. 

L'import fait que créer des notices de livres. Pour chaque livre créé, il vous faudra créer ensuite un exemplaire et renseigner le code barre associé au livre.

