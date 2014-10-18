# Front
Interface AngularJS avec:
1. Une page de recherche de torrent qui amène sur un listing.
2. Un listing avec un status *cached* ou pas pour chaque entrée.
3. Affichage des vignettes zoomables temporellement du film.

# Back
API en PHP qui fait:
1. Un service qui peut pomper un torrent sur le sys si nécessaire et balancer
   une liste de torrents déjà en cache.
2. Un service qui génère les vignettes du film.
3. Un service qui balancer les vignettes au client.

torrent/search
       /add
movie/list
     :id(torrent hash)
movie/chunk/list
           :id(start+duration)
gif/:id(start+duration)
   /create {movie,start,duration}

# Sys
Stockage des films et de leur vignettes.
