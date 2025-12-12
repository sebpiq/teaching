# Notes de présentation - IA : Perspectives

## Introduction

Introduction performance → Automatisation de mon job, mais en fait c'est quoi l'automatisation ?

---

## Automatisation

### Le cycle du capital

Le capitalisme est un système dynamique dont la loi constitutive est l'accumulation de capital.

Quantité d'argent A ---[production]--–> marchandise ---[vente]--–> Quantité d'argent A'

Plus-value = A' - A

Ce processus est cyclique : 

A' ---[production]--–> marchandise ---[vente]--–> A''
A'' ---[production]--–> marchandise ---[vente]--–> A'''
etc.

Ici, on représente un cycle statique idéaltypique, ou à chaque recommencement du cycle, la quantité de capital investie est la même (A). La plus-value extraite à chaque cycle est consommée plutôt que réinvestie.

### L'accumulation

Mais en réalité, il est plus rationnel à chaque cycle de réinvestir une partie de a plus-value engrangée afin d'optimiser le cycle suivant.

Lorsque je pars de A, puis que j'arrive à gagner A' ; au lieu de mettre dans ma poche tout la différence A' - A, je peux faire un pari sur le futur, et décider de la réinvestir pour gagner encore plus au prochain cycle, par exemple je peux investir pour augmenter le volume de marchandises produites, mais je peux aussi investir pour réduire mes coûts de production.

### Compétitivité, innovation et viralité

Cette dynamique de compétitivité a un caractère systémique. Lorsqu'un acteur innove, les autres acteurs qui se battent pour le même marché doivent suivre, au risque de perdre du terrain et éventuellement de disparaitre.

Ainsi dès qu'une firme adopte une technologie permettant de réduire les coûts de production (par exemple en automatisant), la pression concurrentielle pousse les autres acteurs du secteur à imiter cette firme pour préserver leur compétitivité relative.

En conséquence, si une innovation technique apparait possible, peu importe ses effets ou sa désirabilité à long terme, il suffit qu'un acteur la déploie avec succès pour entrainer tout le monde.

### Vagues d'automatisation

À travers les vagues successives d'innovations technologiques, l'histoire des révolutions industrielles montre des épisodes répétés d'automatisation de secteurs entiers : la mécanisation de l'agriculture et du textile au XIXᵉ siècle, la robotisation de l'industrie manufacturière au XXᵉ siècle, ou encore l'informatisation des services financiers, bancaires et assurantiels à partir des années 1970-1980.
Pratiquement à chaque fois, ces épisodes d'automatisations sont accompagnés d'une forme de panique sociale, un phénomène surnommé "automation anxiety".

Prédictions de destruction massive d'emplois à chaque révolution industrielle, accompagnées aussi de prédictions d'un nouvel age d'abondance voir prédictions de Keynes (voir Autor 2014)

---

## Paradoxe de Polanyi et Machine Learning

### Reconnaître un carré

Exercice : Comment peut-on reconnaître un carré ?
Demander au public de proposer des règles pour identifier un carré.

### Reconnaître une chaise

Exercice : Comment peut-on reconnaître une chaise ?
Demander au public de proposer des règles pour identifier une chaise.

[5mn] Diviser le public en groupes de 4-5, leur donner 5 minutes pour produire une description exhaustive des règles qui permettent de décrire une chaise. 

Exemple : 
- C'est un objet en bois
- Il a 4 pieds
- Il a un dossier
- Etc.

[2mn] Demander à un groupe ou deux de partager leur description d'une chaise.

[3mn] Demander au public de trouver un contre-exemple.

### Tag cloud - Types de chaises

Difficile d'écrire un programme lorsqu'on n'est pas capable de décrire précisemment le problème.

L'approche est qu'on va écrire un programme qui va être capable de construire un modèle statistique de ce qui est une chaise et ce qui n'en est pas.

Ceci est l'approche qui est à la base de l'intelligence artificielle moderne.

### Exemple du paradoxe de Polanyi

De manière contre-intuitive, de nombreuses tâches qui nous semblent difficiles (comme réaliser un calcul comptable) sont plus faciles à automatiser que certaines tâches qui nous semblent évidentes (comme marcher ou parler).

Le "paradoxe de Polanyi" formule cette observation de la manière suivante : "we know more than we can tell". C'est-à-dire que de nombreuses actions que nous réalisons quotidiennement utilisent un savoir tacite, incarné (comme marcher, parler ou reconnaître quelqu'un), et nous serions bien en peine de les décrire avec précision. Or, pour automatiser une tâche, il faut justement être capable de la décrire.

De nombreux emplois correspondant à des niveaux d'éducation moyens (production industrielle, assurance, comptabilité, etc.) comprennent justement des tâches procédurales qui sont donc faciles à automatiser, car bien décrites. Alors que les métiers manuels (faire la cuisine, couper les cheveux, etc.) et relationnels (métier du care, etc.), ou les métiers correspondant à des niveaux d'éducation très élevés comme les métiers créatifs ou managériaux résistent à l'automatisation.

### Apprentissage automatique

Au lieu de décrire la procédure pour reconnaître une chaise, on va entraîner un modèle statistique à partir d'exemples.

Le programme va analyser de nombreux exemples de chaises et de non-chaises pour apprendre à distinguer les caractéristiques qui définissent une chaise, sans qu'on ait besoin de les décrire explicitement.

C'est le principe de l'apprentissage automatique (machine learning) qui est à la base de l'intelligence artificielle moderne.

Est-ce qu'avec le machine learning on dépasse le paradoxe de Polanyi ?

### L'image de l'IA

Voici techniquement ce qu'est l'IA : c'est un simple algorithme qui remplit son objectif en opérant une déduction statistique à partir de beaucoup de données, plutôt qu'en suivant des règles explicites programmées par un humain.

Pourtant ça n'est pas du tout comme ça que la société voit l'IA.

Concept en partie culturellement construit, important de comprendre le contexte d'emergence de ces technologies. Pour comprendre pourquoi on les anthropomorphise, important de comprendre avec quelles idéologies elles ont été conçues

---

## Racines culturelles et politiques

Ou "L'idéologie Californienne" (Richard Barbrook et Andy Cameron, 1996)

Mouvement incroyable depuis la pensée radicale des années 60 vers les milliardaires de la tech d'aujourd'hui.

### Années 60-70 : Le communalisme techno-utopiste

Climat d'angoisse nucléaire et bureaucratie technologique. Une génération cherche des alternatives à un monde militarisé et hiérarchique.

Contre-cultures : Mouvement très hétérogène aux influences multiples. Moment de grande fertilité scientifique, artistique, sociale, etc. Notamment inspiré par la pensée de systèmes/réseaux issue de la cybernétique, et une culture de la collaboration transdisciplinaire.

**"New Communalists"** : Se changer soi-même pour changer la société. Accent sur la conscience, l'intimité, les expériences transformatrices. 

**Influences** : Beat, zen, art expérimental, psychédélisme (LSD). Fascination pour Wiener, Fuller, McLuhan.

Pour réaliser ces idéaux, expérimenter avec de nouvelles manières de s'accomplir en société : vague massive de communes rurales et urbaines (1965–1972), jusqu'à plusieurs dizaine de milliers de communes créées, estimations qu'au début des années 70, 750 000 personnes vivaient dans une commune aux US.

Rejet des grands systèmes technologiques mais pas de la créativité technique. Dans beaucoup de ces communes, la technologie est envisagée comme émancipatrice (outil pour tendre vers une harmonie globale, d'expérimentation, d'éveil). Elle permet de réaliser l'utopie cybernétique de connexion à son environnement (les autres comme la nature), monde comme système d'information interconnecté. 

Technologies au sens large : la musique rock (amplifiée électriquement, stroboscopes), le LSD (drogue de synthèse), technologies de communication (radio, calculatrices, etc.).
Informatique : augmenter le champ de conscience de l'individu au même titre que le Lsd.


### Années 60-80 : Naissance du transhumanisme

Naissance dans les années 60-70, contexte technophile de la contre-culture américaine.
Influence de la cybernétique : il n'existe aucune différence ontologique entre l'humain, le vivant et la machine. Tous les trois forment un continuum dans leur effort commun pour lutter contre l'entropie.

Au moment où les machines sont envisagées comme un outil d'émancipation, grandit aussi l'idée que la technologie pourrait permettre à l'humain de dépasser ses limites : super-intelligence, immortalité, conquête de l'espace, rien ne semble hors de portée.

Robert Ettinger, père de la cryogénisation. Premier patient cryogénisé en 1967 James Bedford.

1980s : Formalisation du transhumanisme en tant que mouvement philosophe Max More, fondation du mouvement Extropy.

Utopie techno-scientifique d'une monde où chacun pourrait remodeler sa propre nature. Idée que chaque individu, en véritable self-made-man, peut sculpter librement, par la seule force de sa volonté, sa propre identité, considérée comme entièrement plastique et malléable, et viser un perfectionnement constant. 

Importance de la prothèse, soutenu par le concept de "liberté morphologique", droit de modifier son propre corps.

### Années 80-90 : Le cyberespace

Au cours des années 70, les communes ont échoué. Fort développement de la Silicon Valley. C'est le début de l'ordinateur personnel et des premiers réseaux, certains des anciens communards déplacent leurs aspirations vers les communautés en réseau naissantes.

Années 80 naissance du concept de cyberespace, un nouvel espace non régulé, à la fois promesse de libertés individuelles radicales (liberté d'être, de s'exprimer, de se définir) et nouvel espace de vie en communautés délocalisées. 

Usage prothétique et fusionnel de l'ordinateur

Les courants transhumanistes et anciens communards convergent sur de nombreux points :

- Utilisation des technologies comme prothèses
- Entrepreneuriat et attitude DIY (mouvement des hackers, plus tard biohackers)
- Transdisciplinarité
- Libertarisme
- Élitisme
- Individualisme héroïque

Ces idées façonnent la vision publique et professionnelle de la Silicon Valley et plus largement du numérique.

### Années 90 : Les milliardaires

Explosion de l'Internet au cours des années 90.

John Perry Barlow rédigé la déclaration d'indépendance du cyberespace en 1996 depuis Davos en Suisse. La même année Sergey Brin et Larry Page inventent le PageRank (Google sera fondé en 1998).

La trajectoire de Steve Jobs emblématique de cette mutation de la contre-culture vers le capitalisme numérique.
Adolescent, il était lecteur du whole earth catalog.
En 1974 il part étudier le bouddhisme zen en Inde.
Puis au cours des années 80-90 il est un acteur -clé de la révolution informatique personnelle.

Idéologies Californienne : synthèse entre la contre-culture des années 60 et le capitalisme de la Silicon Valley.

---

## Prospective

Le développement des nouvelles technologies n'est 

Image de l'IA aujourd'hui héritière des visions des pionniers de la Silicon Valley. Anthropomorphisée ("intelligence"), bienveillante, etc.

Garder à l'esprit que les entrepreneurs de la Silicon Valley ne sont pas des oracles, mais des faiseurs qui ont produit le futur qu'ils envisageaient. Quand Sam Altman averti sur l'avènement des intelligences artificielles générales, le présentant comme une inéluctabilité, il faut bien garder en tête que c'est UN PROJET et non une prévision.

### Problème de l'alignement

1. La fonction d'utilité peut ne pas être parfaitement alignée avec les valeurs de l'humanité, qui sont (au mieux) très difficiles à définir.
2. Tout système intelligent suffisamment capable préférera assurer sa propre existence continue [...] – non pour lui-même, mais pour réussir dans la tâche qui lui est assignée.

Un système qui optimise une fonction de n variables, où l'objectif dépend d'un sous-ensemble de taille k<n, fixera souvent les variables non contraintes restantes à des valeurs extrêmes ; si l'une de ces variables non contraintes est en réalité quelque chose qui nous tient à cœur, la solution trouvée peut être hautement indésirable. C'est essentiellement l'ancienne histoire du génie dans la lampe, ou de l'apprenti sorcier, ou du roi Midas : vous obtenez exactement ce que vous demandez, pas ce que vous voulez.

*Of Myths And Moonshine, Stuart Russell, 2014*

Dans Conflit Évitable, Isaac Asimov, 1950, les machines ont décidé que la seule manière de suivre la première loi était de prendre contrôle de l'humanité. 

Première loi : Un robot ne peut porter atteinte à un être humain ni, restant passif, laisser cet être humain exposé au danger.
*Cercle Vicieux, Isaac Asimov, 1942*

### Rupture ou continuité ?

Finalement on entend plus parler des menaces existentielles, et de prophéties technofuturistes, que des impacts concrets et immédiats de l'IA sur nos sociétés.

### Crise environnementale

Système d'IA générative nécessite 33 fois plus d'énergie pour réaliser une tâche donnée qu'avec un logiciel classique.
Source: World Economic Forum, 2024

Consommation des data centers

Paradoxe de Jevons

### Fake news

Cambridge analytica
Réseaux sociaux algorithmes
Monde post-vérité

### Inégalités sociales

Biais raciaux des IA : si on montre que des chaises à 4 pieds alors système pas capable de reconnaître autre chose.
The fragment on machines

### Déterminisme technologique

Faire le lien avec l'aspect viral de l'automatisation.

Loi de Gabor
Le marteau
Les outils conviviaux
