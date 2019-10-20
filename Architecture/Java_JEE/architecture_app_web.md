# Architecture App Web

Generalement 3 couches :
 - Servlet ou controllers : dialogue entre appli et services exterieurs
 - Les Services (code metier)
 - Couche access aux donnees : DAO,files ou External Services
 
 Plus en detail :
  - Servlet ou controllers : dialogue entre appli et services exterieurs
  - Couche de securite : verifier avant et apres l'invocation des sevices que l'utilisateur a les droits
  - Services de haut niveau : code applicatif
  - Services de bas niveau : Valider parametres fournis a la derniere couche et interagir 
    avec les caches de cette couche
  - Couche access aux donnees


Couche servlet ou controleurs :

Decoder les parametres envoyes par le client et rediriger vers les bon services.
Encoder les reponses des services pour etre lu ou affichees par le client


Couche de securite :
Garantir qu'un utilisateur a les droits pour faire tel ou tel action.
Implementation par AOP.
Pour les ACL : implementer une facade de la couche se service, soit utiliser des proxys ou AOP.

Couche service de haut niveau :
Operations metiers effectuées dans l'appli

Couche de service de bas niveau :
Valider les parametres qui sont  transmis à la couche d’accès aux données, 
et éventuellement faire appel à un service de cache comme EhCache.
MBeans pour purger les caches

Couche d'access aux donnees :
Interagir avec les sources de donnees


Exemple:

Couche haute : Spring MVC
couche securite : Spring security
Spring AOP pour autre couches
couche access donnees : Spring Data
