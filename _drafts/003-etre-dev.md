---
layout: episode
number: "006"
title: "Qu'est-ce qu'un développeur ?"
tagline: "Que fait-il ? Avec quelles compétences, outils, attitudes et éthique ?"
img: ""
tags: [LeRubyNouveau, Dev]
duration: "TIME:CODE:LENGTH"
length: "FILE_BYTES"
asset_link: ".mp3"
link: "soundcloud.com/truc"
hosts:
   ynote_hk: Fanny
   flexbox: David
   soveran: Michel
   r3trofitted: Ronan
   loicboutet: Loïc
   abelar_s: Sylvain
actus:
  fosdem: 
   title: FOSDEM
   link: https://fosdem.org/2017/
   comment: "Free & Open Source Developers’ European Meeting"
picks:
  webvr:
   panelist: loicboutet
   title: WebVR API
   link:
   comment: Réalité Virtuelle en Web
  sailorhg:
   panelist: hynote_hk
   title: Sweaters as a Service – Adventures in Machine Knitting
   link: https://www.youtube.com/watch?v=I6071MRIzCA
   comment: Dans son talk à MadisonRuby, Amy Wibowo (@SailorHG) propose de mélanger un hobby (tricoter) et le code, et fait... une API de machine à tricoter ! La programmation doit être fun et créative :)
  impostors_handbook:
   panelist: r3trofitted
   title: The Impostor's handbook
   link:
   comment: Réexplication simple de ce qu'un autodidacte peut rater du cursus classique
  alfred:
   panelist: flexbox
   title: Alfred
   link:
   comment: Spotlight sous stéroïdes - plein de recettes pour tâches communes
  apatternlanguage:
   panelist: soveran
   title: A Pattern Language
   link: https://en.wikipedia.org/wiki/A_Pattern_Language
   comment: livre de Christopher Alexander
  blameless1:
   panelist: abelar_s
   title: Blameless Post Mortem
   link: https://www.pagerduty.com/blog/blameless-post-mortems-strategies-for-success/
   comment: Guide de PagerDuty
  blameless2:
   panelist: abelar_s
   title: Debriefing Facilitation Guide
   link: https://codeascraft.com/2016/11/17/debriefing-facilitation-guide/
   comment: Guide de Etsy
  pompiers:
   panelist: abelar_s
   title:
   link:
   comment:

---

## Qu'est-ce qu'un développeur ?

Sylvain : "quelqu'un qui connaît suffisamment de technique, ET qui résout des problèmes (et pas nécessairement AVEC la technique)"

Fanny : "un technicien qui travaille pour un produit et des enjeux, et qui a les qualités sociales pour travailler en équipe"

Loïc : "retranscrire des contraintes du monde réel dans le monde de la technique" [la Caverne de Platon](https://fr.wikipedia.org/wiki/All%C3%A9gorie_de_la_caverne)

David : "celui qui cherche l'automatisation pour ne pas résoudre deux fois le même problème, et fait gagner du temps sur les tâches qui n'ont pas de valeur"
Et ça peut être simplement de la doc. On n'est jamais tout seul.

Sylvain : face à l'automatisation les gens sont partagés : il y a "c'est tellement compliqué que je veux le faire moi-même, un ordinateur ne peut pas" et "c'est tellement compliqué qu'un humain va se rater, il faudrait qu'un ordinateur le fasse"

Michel : "identifier le problème, son sens, et savoir si c'est un vrai souci."
Résoudre avec du code, c'est créer un nouveau problème. On peut échanger un problème pour un autre, mais cet autre doit être plus facile à gérer.


## Que doit savoir faire un développeur ?

Sylvain : [une matrice de compétences du développeur](http://sijinjoseph.com/programmer-competency-matrix/)
Imparfaite et à adapter, mais un bon premier pas pour lister des compétences et des savoirs : pour se situer, s'auto-évaluer, voir ce qu'on peut apprendre ensuite.

* computer science : théorie, structures de données, algos
* engineering : méthodes de travail
* programming
* expérience : j'ajouterais l'humain
* connaissances pures

Loïc et Fanny : [un MindMap des compétences pour Rails](https://www.codefellows.org/blog/this-is-why-learning-rails-is-hard/)
Issu d'un article "pourquoi Rails c'est compliqué".

* Outils : OS, command line, IDE/text editor, git...
* SQL, WWW, déploiement
* Ruby & RubyGems
* Rails, MVC, conventions...
* Software Engineering, tests

Permet aussi de rappeler ce qu'on "sait sans le savoir" et de rappeler ce qu'il y a dans l'état de l'art, et ce qu'on pourrait ou devrait expliquer à des collègues. 

Ronan : les savoir-être
[Pratiques d'un développeur agile](https://pragprog.com/book/pad/practices-of-an-agile-developer)
Qualités morales et attitudes : modeste, courageux, humble, travail en équipe...

Michel : générosité

Sylvain : à l'inverse il y a les [Trois Vertus](http://wiki.c2.com/?LazinessImpatienceHubris) du développeur "Paresse, Impatience et Hubris".

## Éthique

Et les remarques suite au Scandale VolksWagen, me rappellent [the Order of the Engineer](https://en.wikipedia.org/wiki/Order_of_the_Engineer) et leur [serment](http://www.order-of-the-engineer.org/?page_id=6).
ERRATUM : c'est un anneau d'acier inoxydable porté sur le petit doigt.

Ronan : oui c'est aussi dans la conf de UncleBobMartin [The Future of Programming](https://www.youtube.com/watch?v=ecIWPzGEbFc)

Loïc : je pense aux Fake News et l'esprit startup "réussir à tout prix", "fake it till you make it" est très imprégné dans la culture dev :/

Sylvain : à écouter, l'excellent [Planet Money - Fake-News King](http://www.npr.org/sections/money/2016/12/02/504155809/episode-739-finding-the-fake-news-king) montre la responsabilité des revenus par la pub.
Et la contre-attaque de [@slpng_giants](https://twitter.com/slpng_giants).

## Attitude

Loïc : difficile d'avancer et avoir les bonnes infos dans une ambiance délétère.

Fanny : la bienveillance et la responsabilité en équipe.
L'échec de l'un c'est l'échec de toute l'équipe.

Sylvain : le métier de développeur c'est de débugguer la spec.
C'est difficile de le faire sans être bloquant, arrogant, méchant.
Il faut apprendre à communiquer, étudier, proposer.
Et avancer en sachant qu'on est faillible.

Fanny : important de pouvoir expliquer et parler aux non-tech.

David : [the starter, architect, debugger and finisher](http://jacquesmattheij.com/the-starter-the-architect-the-debugger-and-the-finisher).
Dans les entretiens d'embauche, ça permet d'avoir leur rapport au code et aux projets. Chacune a ses avantages et inconvénients.

Michel : [A Pattern Language](https://en.wikipedia.org/wiki/A_Pattern_Language) de Christopher Alexander, contient plein d'éléments mais à son grand dam c'est "le moins important" qui a été retenu.

Sylvain : beaucoup d'auteurs finissent par avoir cet avis sur l'écrit qui les a rendus célèbres : GoF (livre des Design Patterns), la Conway's Law, DDD et Agile Manifesto.
