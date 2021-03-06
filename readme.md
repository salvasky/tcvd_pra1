## **Tipologia i cicle de vida de les dades - Pràctica 1**

----
# **Mercat de les flors - Reflexions entorn del confinament**

**Components del grup:**

Joan Manuel López Ruiz <jlopezruiz012@uoc.edu>

Salvador Sanchis Beneseit <ssanchisb@uoc.edu> 

----

El lloc web sobre el qual hem triat treballar és el següent:

https://mercatflors.cat/blog/reflexions-entorn-dun-confinament/

És una pàgina web anomenada "Reflexions entorn d'un confinament", publicada pel 
Mercat de les Flors de Barcelona, i recull un seguit d'articles que el teatre 
va encarregar a diverses artistes en l'àmbit de la dansa contemporània
durant el primer confinament provocat per la 
Covid-19. Els articles es van publicar durant els mesos de maig i juny del 2020.

La pàgina a la qual accedim amb el nostre codi de scraping és la pàgina d'accés
als articles, amb un quadre resum per cada article, on apareix el títol de 
l'article (que és 
en realitat el nom de l'artista que l'escriu), amb una foto de l'artista, la 
data de publicació, i una frase pertanyent al text de l'article. Per llegir 
cada article cal clicar sobre el quadre resum, i així accedim a les seves
pàgines respectives. Quan accedim a la pàgina principal, només hi apareixen
els primers 4 quadres resum, i si fem un scroll els altres quadres resum es
van carregant, fins a arribar a un total de 21 quadres.

El dataset que generem amb l'script 'mdf.py' conté
el títol de cada article (nom de l'artista),
la data de publicació, la url de la foto de l'artista, el text complet i 
la frase extreta del text que apareix al quadre-resum.

Previ a la generació del dataset, l'script mdf.py té les següents funcionalitats:

* Scrape sobre la pàgina principal amb Beautiful Soup.

* Navegació a través de l'scroll infinit de la pàgina amb webdriver de Selenium
per tal d'accedir als enllaços de tots els articles.

* Extracció de la informació relativa a cada article: títol, data,
  (URL de la) foto, frase extreta de l'article.

* Scrape de les pàgines de cadascun dels articles dels artistes per accedir al text íntegre 
i incorporar-lo al csv resultant.

* Emmagatzematge en un directori de les fotos de cada article en format jpg.

* Creació i emmagatzament d'una imatge "tag cloud" en format .png amb les paraules més utilitzades
d'un dels articles.


