---
title: 'Comprendre la matière numérique'
...

## La boite noire

<video src="videos/damasio.mp4"></video>

[Blast - Interview avec Damasio : L'IMAGINAIRE CAPITALISTE EST DEVENU RINGARD, IL SE FISSURE DE PARTOUT](https://www.youtube.com/watch?v=Y8SpcxR6FjQ)

> Les symptômes d’une crise planétaire qui va s’accélérant sont manifestes. On en a de tous côtés cherché le pourquoi. J’avance pour ma part l’explication suivante : la crise s’enracine dans l’échec de l’entreprise moderne, à savoir la substitution de la machine à l’homme. Le grand projet s’est métamorphosé en un implacable procès d’asservissement du producteur et d’intoxication du consommateur. 
> 
> La relation de l’homme à l’outil est devenue une relation de l’outil à l’homme. Ici il faut savoir reconnaître l’échec. Cela fait une centaine d’années que nous essayons de faire travailler la machine pour l’homme et d’éduquer l’homme à servir la machine. On s’aperçoit maintenant que la machine ne « marche » pas, que l’homme ne saurait se conformer à ses exigences, se faire à vie son serviteur. Durant un siècle, l’humanité s’est livrée à une expérience fondée sur l’hypothèse suivante : l’outil peut remplacer l’esclave. Or il est manifeste qu’employé à de tels desseins, c’est l’outil qui de l’homme fait son esclave. La dictature du prolétariat et la civilisation des loisirs sont deux variantes politiques de la même domination par un outillage industriel en constante expansion. L’échec de cette grande aventure fait conclure à la fausseté de l’hypothèse. 
> 
> La solution de la crise exige une radicale volte-face : ce n’est qu’en renversant la structure profonde qui règle le rapport de l’homme à l’outil que nous pourrons nous donner des outils justes. L’outil juste répond à trois exigences : il est générateur d’efficience sans dégrader l’autonomie personnelle, il ne suscite ni esclaves ni maîtres, il élargit le rayon d’action personnel. L’homme a besoin d’un outil avec lequel travailler, non d’un outillage qui travaille à sa place. Il a besoin d’une technologie qui tire le meilleur parti de l’énergie et de l’imagination personnelles, non d’une technologie qui l’asservisse et le programme.


[Ivan Illich - La convivialité (1973)](https://archive.org/details/illich-convivialite)


## L'ordinateur

-> Un ordinateur est-il complexe ou compliqué ?

<img title="a title" alt="Alt text" src="images/know-how-computer.jpg">

[WDR Papiercomputer (1983)](https://cstaecker.fairfield.edu/~cstaecker/files/machines/filer.php?name=knowhowarticle.pdf)

5 Instructions :

```txt
+ [reg] : ajoute 1 au registre [reg]
- [reg] : soustrait 1 au registre [reg]
J [ligne] : saute à la ligne de code [ligne]
0 [reg] : si la valeur dans le registre [reg] est 0, saute une ligne de code et continue. Sinon, ne fait rien et passe à la ligne suivante.
stop : fin du programme
```

- Exercice 1 : Vider le registre 1
- Exercice 2 : Additionner registres 1 et 2, mettre réponse dans registre 1
- Exercice 3 : Démarrer avec un nombre dans le registre 1, terminer avec 2 fois ce nombre dans le registre 2.
- Exercice 4 : Démarrer avec un nombre N dans le registre 1, terminer avec 0 dans le registre 2 si N est pair, ou 1 dans le registre 2 si N et impair

-> quelles fonctions peut-on programmer avec le WDR Papiercomputer ?

-> Comment des applications d'une complexité bien plus élevée emergent-elles d'une unité de calcul aussi simple ?

**Refs**

- [Der Know How Computer (WDR Papiercomputer) - Paper Computers #1](https://www.youtube.com/watch?app=desktop&v=Z27KQiBnkJI)



## La donnée

-> Un fichier est un nombre

- [Le paradoxe du singe savant (aka “Infinite monkey theorem”)](https://i-dat.org/2002-generator/)
- [pifs](https://github.com/philipl/pifs)

-> Editeur hexadécimal en ligne : https://hexed.it/


### Matière numérique

Écouter un fichier texte :

```bash
cat /var/log/kern.log | aplay -c2 -r 4000 -f MU_LAW
```

Écouter le traffic réseau :

```bash
sudo tcpdump -vvv | aplay -c2 -r 2000 -f FLOAT_LE
```

Écouter une image :

- télécharger et installer [Audacity](https://www.audacityteam.org/)
- importer une image BMP : 
    - sélectionner `File -> Import -> Raw Data`
    - choisir l'image
    - choisir les options suivantes : 
        - `U-Law`
        - `Little-endian`
        - `1 Channel`
        - laisser les autres options avec leurs défauts
    - cliquer sur `Import`

Lui appliquer des effets audios :

- Dans audacity, séléctionner un partie en milieu de l'image, en évitant bien les bords
- Choisir `Effect -> Reverb`, pius appliquer l'effet
- Export le fichier à nouveau comme image :
    - Choisir `File -> Export -> Export audio`
    - sélectionner le format `Other uncompressed files`: 
        - Header : `RAW (header-less)`
        - Encoding : `U-Law`
    - Sauver le fichier avec l'extension `.bmp`


-> Si on applique un effet sur la fin ou le début de l'image, l'export est une image inutilisable ... pourquoi ? 



### Format de fichier : example du GIF

-> Le format d'un fichier est arbitraire et décidé par les développeurs de l'application vouée à lire ce fichier.

Pour faire du data-bending sur un GIF animé : 

- importer un fichier animé GIF dans l'éditeur hexadécimal
- trouver l'octet 11 : 
    - vérifier que le GIF contient une table globale de couleurs -> le premier bit de l'octet 11 est `1`.
    - vérifier que la taille de la table est 256 -> les 3 bits suivants sont `1 1 1`
- [copier l'une des tables de couleurs suivantes](./glitching-gifs.html)
- la coller sur l'octet 14 : 
    - vérifier qu'on est bien en mode "overwrite"
    - vérifier qu'on prend bien de la donnée hexadécimale



### Un programme c'est aussi de la donnée

Firefox corrompu : [https://faultlore.com/glitch/](https://faultlore.com/glitch/)

Code binaire de Firefox : 

```bash
xxd /snap/bin/firefox | less
```


**Refs**

- [What's in a GIF](https://giflib.sourceforge.net/whatsinagif/bits_and_bytes.html)
- [Glitching gifs](http://blog.animalswithinanimals.com/2014/10/databending-and-glitch-art-primer-part.html?m=1)
- http://nickbriz.com/databending101/
- https://github.com/topics/databending



## Le code

-> Le code c'est l'interface de programmation de l'ordinateur.

-> Code ouvert (open source), VS code fermé (cf code binaire de Firefox VS code source de Firefox)


### Le web, plateforme ouverte par excellence

<img title="a title" alt="Alt text" src="images/first-www.gif">

[le World Wide Web - www Le premier “navigateur Internet” implémenté par Tim Berners-Lee, 1990](https://home.cern/fr/science/computing/birth-web/short-history-web)


### Visualiser le code d'une page

-> Ouvrir la "developer console" sur son navigateur : Firefox ou Chrome : ctrl + shift + c / Cmd + Option + c sur mac

Comment downloader du contenu sur instagram : 

- Ouvrir Instagram dans la navigateur
- Ouvrir la console developeurs
- Cliquer sur la petite icone "pick an element" en haut à gauche de la console.
- Sélectionner l'image à télécharger
- trouver dans l'arbre des éléments html l'élément `<img>` correspondant.
- copier son attribut `src`
- ouvrir cette url dans un autre onglet

Comment lire les articles de certains journaux sans avoir à s'abonner

- Ouvrir la page du [New Yorker](https://www.newyorker.com)
- Sélectionner un article (après quelques lectures, le site va vous demander de vous abonner)
- Ouvrir la console dévelopeurs, onglet "Debugger"
- Repérer le bouton "pause" à droite
- Recharger la page, puis avant l'apparition de la popup d'abonnement, appuyer sur "pause"


### Jouer avec le contenu d'une page

Extensions Chrome : 

- [Crazy page](https://github.com/Steven-Roberts/Crazy-Page)
- Do It ! Shia Labeouf
- libdoge

Rendre des pages web plus intéressantes en executant du code directement dans la console :

- Copier coller dans la console [les fonction suivantes](./page-fuckups.html)
- Essayer de lancer l'une des fonctions en copiant collant son code (par exemple : 
```javascript 
shake('div', 100, 1, 0.05, false)
```
)