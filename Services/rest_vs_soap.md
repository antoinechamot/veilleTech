## SOAP VS REST


SOAP :
 - c'est un protocole *
 - SOAP utilise des interfaces de service pour exposer la logique metier
 - Normes strict a suivre
 - SOAP necessite + de bande passante et de ressources *
 - SOAP definit sa propre securite WS-Security
 - Format XML uniquement
 - Possibilite d'utiliser des WSDL pour definir le contrat de service
 - SOAP inclus un mecanisme de rejeu en cas d'echec



REST : (GET, POST,PUT, DELETE)
 - c'est un style d'architecture
 - Rest utilise l'URI pour exposer la logique metier
 - Pas de norme strict
 - Les web services heritent des mesures de securite du transport utilise (SOAP,HTML,...)
 - Differents formats autorises HTML,XML,JSON
 - REST peut disposer d'une solution de mise en cache *
 - Better spped and scalability
 
 
 JAX-WS est l'api pour les deux
 REST est prefere
 

REST IS THE DEFAULT SOLUTION because :
 - consumes less bandwidth, it is compatible with hhtp.
 
HOWEVER SOAP offer additional security