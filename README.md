## Introduction

Cette bibliothèque C est une collection open source d'outils pour le langage de programmation C.  
Le projet est en développement continu, avec des fonctionnalités ajoutées et révisées continuellement au fil du temps.  

## Compilation

Si vous sauvegardez le répertoire libeom dans votre emplacement d'inclusion par défaut, il n'y a pas besoin de compiler quoi que ce soit ; cependant, un makefile est fourni pour permettre la compilation de libeom en une bibliothèque statique contenant tous les sous-modules, des sous-modules individuels, ou les deux. La configuration la plus simple est de compiler les deux avec la commande :

```
make
```

Cela générera une bibliothèque statique pour libeom dans son ensemble, ainsi que des bibliothèques statiques pour chacun des sous-modules individuellement. Si vous souhaitez seulement compiler la bibliothèque statique de niveau supérieur, utilisez :

```
make Main
```

Si vous souhaitez compiler une bibliothèque statique pour seulement une partie de libeom, vous devrez utiliser la commande spécifiée pour cette section. Vous pouvez trouver la commande dans le README de ce sous-module, ou dans la table des matières ci-dessous.

Après avoir utilisé l'une des commandes make mentionnées ci-dessus, il est recommandé d'exécuter :

```
make clean
```

Pour supprimer les fichiers objets résiduels.

## Inclusion

La façon la plus simple d'importer la bibliothèque est simplement de télécharger le dossier du projet et de le copier dans votre projet, puis de référencer les fichiers d'en-tête désirés. Vous devrez utiliser des crochets ou des guillemets selon la façon dont vous comptez utiliser la bibliothèque, mais la documentation est écrite comme si libeom était sauvegardé dans votre chemin d'inclusion par défaut.

```
// Si dans le chemin d'inclusion par défaut :
#include <libeom.h>
// Si dans le même répertoire que votre projet :
#include "libeom/libeom.h"
```

Si vous utilisez libeom comme une bibliothèque statique, n'oubliez pas d'inclure le fichier .a désiré dans votre commande :

```
gcc my_project.c libeom/libeom.a
```

Si seulement une section de la bibliothèque est désirée, cette section seule peut être incluse, et des bibliothèques statiques sont fournies pour chaque sous-module.  
Encore une fois, utilisez l'instruction d'inclusion et paramétrez la bibliothèque statique (si applicable) :

```
#include <libeom/DataStructures/DataStructures.h>
```

```
gcc my_project.c libeom/DataStructures/DataStructures.a
```

Puisqu'il y a de nombreux sous-modules, ce fichier servira simplement de table des matières pour ce qui est inclus dans la bibliothèque. 

## Contenu

Pour une documentation spécifique sur les composants, consultez le README inclus dans les répertoires des sous-modules.  


### Structures de Données

**Emplacement :**

```
libeom/DataStructures
```

**Inclusion :**

```
#include <libeom/DataStructures.h>
```

#### Composants

**Commun**

* Nœud

**Dictionnaire**

* Entrée
* Dictionnaire

**Listes**

* ListeLiée
* File

**Arbres**

* ArbreRechercheBinaire

### Réseau

**Emplacement**

```
libeom/Networking
```

**Inclusion**

```
#include <libeom/Networking.h>
```

#### Composants

**Nœuds**

* Serveur
* ServeurHTTP

**Protocoles**

* RequêteHTTP

### Systèmes

**Emplacement**

```
libeom/Systems
```

**Inclusion**

```
#include <libeom/Systems.h>
```


