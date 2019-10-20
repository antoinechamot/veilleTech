# Design pattern

## Pattern Factory

Fournit une interface pour créer des objets mais laisse les sous classes décider quelle classe instancier.

Product <- ConcreteProduct
Creator(FactoryMethod) <- ConcreteCreator


## Pattern Abstract Factory

Fournit une interface pour créer des familles  d'objets associés ou dépendants sans spécifier 
leur classes concrètes. Une Factory qui crée d'autre factory

AbstractFactory(CreateProductA,CreateProductB)<-ConcreteFactory1, ConcreteFactory2
AbstractProductA<-ProductA1,ProductA2
AbstractProductB<-ProductB1,ProductB2

## Pattern singleton
Assurer qu'une classe n'a qu'une seule instance et fournit un point d'acces global à celle ci

Singleton (static Instance() static uniqueInstance)

## Pattern Decorator
Attribut une responsabilite dynamique à un objet.
Ce pattern consiste à utiliser la composition et limiter l'heritage ppour simplifier les relations d'objets.
Ils sont plus facile à mettre à jour et gérer.


##Pattern iterator
Moyen d'accéder et de parcourir les éléments d'une collection de la même manière, 
quelque que soit le type de collection, que ce soit un tableau, une liste de dictionnaires ou autre

##Pattern observer
Definit une dépendance un-à-plusieurs entre des objets, 
de sorte que lorsqu'un objet change d'état, tous ses dépendants sont notifiés et mis à jour automatiquement.

##Facade
Facade englobe un system complexe derriere une interface simple.