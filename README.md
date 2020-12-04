Web audio local smartphone webapp 2ème semaine de décembre
SP VR RI?

client / serveur
bidirectionnalité du web
web local vs global

webpd / js puredata (2012)
topologie

** intro aux réseau pour artistes : SEB
** portail captif
** capteurs RI
** composition sonore
** corpus de sons smartphones

Description

Nom: Son et réseaux numériques - potentiel artistique et perspectives critiques

Le but de ce cours de 3 jours, sera de vous transmettre les outils pour réaliser vos propres installations artistiques en réseau. Nous travaillerons avec le son comme medium principal, mais les compétences acquises seront aussi utiles pour d'autres media (vidéo, web, sculptures interactives, ...). 

Les matinées seront consacrées à un cours en visio dans lequel nous aborderons le concept de réseaux et les technologies qui les font fonctionner sous un aspect théorique et critique. Le cours sera emaillé de nombreux exemples et expériences que nous pourrons réaliser ensemble à distance (il est recommandé de se connecter sur son ordinateur portable et de se munir en plus d'un smartphone). Les connaissances de base que vous acquiererez (qu'est ce qu'une adresse IP, un protocole, un client / server, ...) vous serviront non seulement pour penser vos projets, mais seront aussi un point d'entrée vers une conscience élargie des enjeux sociaux et politiques représentés par les réseaux numériques et tout particulièrement par l'Internet. Comment circulent les données, qui peut y accéder, qui contrôle les infrastructures, est-il possible se les réapproprier grâce au DIY et à l'utilisation de logiciels libres?

Les après-midi seront consacrés à l'experimentation, et nous réaliserons ensemble plusieurs projets. Nous travaillerons sur la web-radio radiobal, que nous diffuersons pour l'occasion sur un réseau wifi local. Nous mettrons en places des installations audio-visuelles en réseau grâce au protocole de communication OSC. Et enfin, nous laisserons un temps d'expérimentation et de discussion libre qui permettra aux étudiants de penser des projets qu'ils aimeraient réaliser avec ces technologies.



ANCIENNE VERSION : Le but de ce cours de 3 jours (?), sera de vous transmettre les outils pour réaliser vos propres installations en réseau. Nous travaillerons avec le son comme medium principal, mais les compétences acquises seront aussi utiles pour d'autres media (vidéo, web, sculptures interactives, ...). En plus de la transmission de techniques concrètes et directement applicables pour vos projets artistiques, nous aborderons le concept de réseaux et les technologies qui les font fonctionner sous un aspect plus théorique et critique. Ces connaissances de base (qu'est ce qu'une adresse IP, un protocole, un client / server, ...) vous serviront non seulement pour penser vos projets, mais seront aussi un point d'entrée vers une conscience élargie des enjeux sociaux et politiques représentés par les réseaux numériques et tout particulièrement par l'Internet. Comment circulent les données, qui peut y accéder, qui contrôle les infrastructures, est-il possible se les réapproprier grâce au DIY et à l'utilisation de logiciels libres?




Objectifs
- Apprendre à mettre en place (et débugger) un réseau wifi local (sous openWRT?)
- Apprendre à connecter des applis existantes (Pd, Ableton live, etc ...) avec OSC sur un réseau local Wifi

Cours "théorique"

Infrastructure
- Physicalité des réseaux, cables transatlantiques
- IP protocol
Qu'est-ce qu'une addresse IP ? A quoi ça sert  ?
Comment sont attribuées les addresses IP ? Qui a le contrôle des addresses IP sur l'Internet ? Qu'est ce que ça signifie d'un point de vue de ma vie privée ?
Pourquoi mon téléphone et mon ordi ont la même IP ? Pourquoi elle change si je passe mon téléphone en 3G VS wifi ?
Glitch réseau
- Internet VS réseau local

-> Accessibilité : Starlink / wigle.net, etc ...
-> Pings
-> Petit IP crawler en ligne?
-> Traceroute
-> DNS lookup / reverse lookup 

Encodage
- Octet, différence analogique / numérique (continu / discontinu)
- Binaire VS Morse code
- MP3 => Shannon encoding (explication de 44100 hz), quelle est la différence wav / mp3 ?
- aplay listen, data bending (audacity)
- Formats audio WAV structure (header + PCM data), mp3. Lossy vs lessless (hands on experiment with data bending).
- Exemples / tutoriels databending / datamoshing : 
    Databending tutorial series : https://www.youtube.com/playlist?list=PL7w4cOVVxL6HfT-FoqQ1ukW2G__l0fTr6
    Datamoshing, tutoriels en français (un peu vieux) : https://ressources.labomedia.org/le_datamoshing
- Datamosh
    https://www.youtube.com/user/burntfritter/videos
    https://www.youtube.com/watch?v=gcppKXM12eY
    https://www.youtube.com/watch?v=ybdHLxsIFsE
    https://www.youtube.com/watch?v=gYMBUIR7C9o

Protocoles
- Alphabet sémaphore : https://fr.wikipedia.org/wiki/Alphabet_s%C3%A9maphore
- MIDI
- OSC
- DMX
- IP / TCP-UDP  ====> glitch (sonores, vidéos)

Client / serveur
- Centralisation / décentralisation
- WhatsApp VS Facebook
- FB data dump
- "l'échange" - Clint Eastwood télécharger extrait

Son sur le web
- Audio streaming
- HTML5 audio
- Web Audio

Références 
- OSI layers
- Internet of Things Hacks https://www.vice.com/en/article/nzqayz/this-teen-hacked-150000-printers-to-show-how-the-internet-of-things-is-shit
- Facebook confirms that it tracks how you move mouse on the computer screen https://www.indiatoday.in/technology/news/story/facebook-confirms-that-it-tracks-how-you-move-mouse-on-the-computer-screen-1258189-2018-06-12#close-overlay
    