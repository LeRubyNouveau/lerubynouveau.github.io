---
layout: episode
number: "004"
title: "Migrations"
tagline: "Migrer de "
img: ""
tags: [LeRubyNouveau, Bienvenue]
duration: "TIME:CODE:LENGTH"
length: "FILE_BYTES"
asset_link: ".mp3"
link: "soundcloud.com/truc"
hosts:
   r3trofitted:
   _toch:
   wondersonja:
   soveran:
   abelar_s:
actus:
  ruby24:
   title: Ruby 2.4 
   link: https://www.ruby-lang.org/en/news/2016/12/25/ruby-2-4-0-released/
   comment: Sortie de Ruby 2.4 à Noël :)
picks:
  gildedrose:
   panelist: _toch
   title: Code Kata Gilded Rose
   link: https://github.com/jimweirich/gilded_rose_kata
   comment: Pour animer des Code Retreats
  amontourdeprogrammer:
   panelist: wondersonja
   title: À mon tour de programmer
   link: http://amontourdeprogrammer.fr/
   comment: Formation au code de 12 femmes, partenariat La Mairie de Paris
  dojo:
   panelist: abelar_s
   title: Dojo de Code & CodeRetreats
   link:
   comment: Trouvez ce genre d'événements dans votre région :)
  gunsNroses:
   panelist: r3trofitted
   title: Last of the Giants
   link: https://www.goodreads.com/book/show/32179238-last-of-the-giants
   comment: biographie des Guns & Roses
  :
   panelist: soveran
   title: Spec-ulation - par Rich Hickey
   link: https://www.youtube.com/watch?v=oyLBGkS5ICk
   comment: Talk de Rich Hickey 
---

## Ruby
Ruby 2.4 est sorti !

Ronan : d'habitude c'est toujours le cadeau, là quelques warnings.

Christophe : depuis 1.9 ça se passe toujours bien.

Ronan : c'est surtout l'uniformisation des Bignum Fixnum qui met des warnings dans les gems. Pour 1.9 c'était la gestion des strings et unicode.

Sylvain : JRuby le cadeau de perf ;)

## Rails
Shopify : entre 2 et 4 personnes pendant un an pour passer à Rails 5.0
Ils ont l'argent et les Core members.

Sylvain : le `permit` est le plus gros souci pour ceux qui migrent.

Ronan : de 3 à 4, facile.
Rythme des releases de Rails : grosses MàJ tous les 6 à 18 mois, pas toutes les 6 semaines comme Ember. Le temps pris c'est aussi et surtout de profiter des nouveautés.

Sylvain : Rails rattrape souvent des usages établis, ou des gems populaires.
Par exemple le OR arel était très attendu, on retire des verrues surtout.

Christophe : Rails 3 à 4 c'était assez gros.
Beaucoup de découvertes dans les petites ramifications.
À l'époque il y avait un livre avec les points d'attention.

Sylvain : oui et des scripts de deprecation / migration automatique.
Ronan : les Rails Guides incluent toujours des guides d'upgrade, rake update aussi par exemple.

Sonia, Ronan : ça implique que toute l'équipe suive les Best Practices.

Michel : rien que pour la sécurité, tu dois tout embarquer.

Sonia : à quoi il faut penser pour une migration ?

Christophe : c'est comme du refactoring : la couverture de test.

## Dépendances

Ronan : passer en revue toutes les dépendances :
- j'attends qu'elle soit prête
- j'essaie de m'en passer

Sylvain : dès le début, choisir et faire attention à la... dépendance,
aux dépendances. Est-ce acceptable ? Tentaculaire ? Lourd ? Justifié ?

Sonia : ça nous est arrivés, on a dû réécrire une partie de la gem

Ronan : nous aussi, entre les périodes de bascule Rails 2 et 3,
on a choisi un fulltext-search et on a dû attendre longtemps qu'elle soit OK.

Christophe : https://www.deppbot.com/faq

Ronan : Rails te pousse à aller de l'avant, ne pas être complaisant avec son code.

Michel : il faut faire attention à ne pas être trop interdépendant

Sylvain : Rails est mature, son architecture est stable, il est resté dans le cadre et je ne suis pas trop contraint. Un junior se retrouverait aujourd'hui dans du code très ancien.

Christophe : http://bundler.io/v1.14/bundle_viz.html

Sylvain : il faudrait synchro avec DeppBot :)

Ronan : [Gemnasium](https://gemnasium.com/) fait ça !
On fait des bundle outdated réguliers.
C'est aussi dommage qu'une gem évolue et qu'on n'en profite pas,
du coup on regarde un peu si ça vaut toujours le coup, si on est en ligne.

Sonia : est-ce que tout le monde a le temps de faire ça ?
Dans des contextes d'équipe ou d'argent serré, que faire ?

Sylvain : c'est comme de l'hygiène : tu peux le zapper une fois, deux fois... mais il faut que ce soit régulier pour éviter les catastrophes, sinon ça finit par être dix fois plus cher.

Sonia : combien de temps alors ?

Ronan : 30mn max par semaine, souvent c'est 10.

Christophe : c'est selon la phase de projet.
Et puis il faut aussi avoir la clairvoyance de savoir si on est en train de faire de l'acharnement thérapeutique.
Dans une phase de prototype, par exemple, l'équilibre n'est pas le même.

Ronan : on peut aussi utiliser vendor.
Quand une gem n'évolue plus, on veut s'en débarrasser,
on va garder les "vivantes" dans le Gemfile et on s'engage à les maintenir,
on va garder les "moribondes" dans vendor avant de s'en débarrasser.

Christophe : et réévaluer le besoin, prendre une gem plus simple
Sylvain : ou forker la gem
Michel : avoir trop de dépendances est une faiblesse de la gem

Sylvain : il y a les mises à jour "gratuites" (pas de changement d'interface),
et la mise à jour "payante" où les développeurs doivent changer.
Rails a fait le choix d'une archi stable,
Ember a fait le choix d'un dev drivé par "ce qui leur semble utile",
et sont clairs avec le fait que c'est à vous de changer s'ils cassent tout.
Depuis ils ont un 2e contrat : livrer toutes les 6 semaines. C'est clair.
Angular a fait un coup moins réglo : promettre Une Vraie Voie
puis arrêter et "tuer" Angular 1 au profit d'Angular 2, assez différent.

Christophe : oui c'est appréciable d'avoir des mainteneurs lucides
et transparents sur les directions et les contraintes.

Ronan : Shopify ont une approche agréable de migration progressive :
10% de nos machines, puis 30% sur la nouvelle version, puis...

Sylvain : parfois ton archi est directement conçue comme cela,
ça te permet d'avoir une appli modulaire et des contrats simples
et bien délimités, et ça facilite les changements

Ronan : attention tu pars sur les microservices :)

Sylvain : oui mais pas seulement, juste de domaines bien découpés.
Pour la formation d'un junior par exemple c'est pratique.

Ronan : finalement si tu as "peur" de migrer c'est un signe :
il faut se demander pourquoi on a peur, et savoir que c'est pas bon.

Sylvain : Kent Beck disait "ne faites pas de changement difficiles,
faites du travail pour que le changement devienne facile,
puis faites le changement facile"

Sonia : mais on n'a pas toujours la direction des projets, comment faire ?

Sylvain : c'est du feeling et des contrats clairs, à voir en avançant

Christophe : récemment sur [Hanami](http://hanamirb.org/) j'ai eu ce plaisir,
ils ont changé mais sont restés sur des contrats clairs et une archi donnée.

Sylvain : pour reprendre le sujet de Sonia, finalement le junior
lui-même n'aura pas à faire ces choix : on ne le lui demande pas.
Et on attendra du senior dev non seulement qu'il le sache, mais
qu'en plus il sache communiquer au management que ce temps, cette hygiène,
ces choix sont faits car ce sont des décisions business.

Sonia : j'aime beaucoup cette idée que chacun a un contrat envers les autres

Christophe : on est engagés pour notre expertise, on peut être écoutés.
