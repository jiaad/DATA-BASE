Récupérer tous les albums


Récupérer tous les albums dont le titre contient "Great" (indice)
2/ SELECT * FROM tracks WHERE ((Name) LIKE '%great%')

----------------------------------------------------------

Donner le nombre total d'albums contenus dans la base (sans regarder les id bien sûr)
3: SELECT count(*) FROM albums
----------------------------------------------------------
Supprimer tous les albums dont le nom contient "music"
4/DELETE FROM albums WHERE Title LIKE '%music%'; 
----------------------------------------------------------

Récupérer tous les albums écrits par AC/DC
5/SELECT * FROM albums WHERE ArtistID LIKE '1'

----------------------------------------------------------

Récupérer tous les titres des albums de AC/DC
6/

Récupérer la liste des titres de l'album "Let There Be Rock"
7/SELECT Name  FROM tracks WHERE AlbumId LIKE '4' 

Afficher le prix de cet album ainsi que sa durée totale
9/SELECT SUM (UnitPrice) FROM tracks WHERE AlbumId LIKE '4';
====================================================
9.A/sqlite> SELECT SUM(Milliseconds)/60000 FROM tracks WHERE AlbumId LIKE '4';

===========================     ==========================

============================    ===========================



Afficher le coût de l'intégralité de la discographie de "Deep Purple"
10/ SELECT SUM (UnitPrice) FROM tracks WHERE AlbumId LIKE '59'+ '61';


---------------------------------------------------------

Créer l'album de ton artiste favori en base, en renseignant correctement les trois tables albums, artists et tracks
