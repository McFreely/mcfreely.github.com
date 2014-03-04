---
layout: post
title: RDC - République Démocratique du Cinéma
image: /images/banners/liberte.jpg
alt: Liberté guidant le peuple
category: Technique
status: Draft n°2
tags: Révolution
---

Mon nouveau projet. Un site de critique cinéma vraiment démocratique. Comment cela est-il possible? Avec l'analyse de sentiments de milliers de tweets, tout simplement. Cet article est le premier d'une longue série, un introduction en quelque sorte.

### L'inception

J'ai longtemps voulu jouer avec différentes techniques de processing de language naturel (NLP) pour quelques raisons. Premièrement, parce que c'est vraiment cool. Etant légèrement un geek de litérature, dès lors qu'il m'est possible de combiner le code et la prose, c'est tout de suite un grand plaisir. Deuxièmement, en travaillant sur quelques projets en pre-production (c'est-à-dire des idées dans un carnets), je me suis rendu compte que beaucoup des techniques sous-jacentes revenait souvent à la NLP. L'une d'entre elles étant l'analyse de sentiment (AS). L'AS est pratique, c'est une application directe des concepts des théories de NLP. 

C'est durant la même période que j'ai remarque le manque cruel de bon site de critique cinéma en français. A part Allociné qui est désormais complètement contaminé par les pubs, il n'y a presque rien. Pas de RottenTomatoes (RT), pas de Flixter, rien du tout.
L'idée de créer quelque d'équivalent à RT fut donc evidénte, mais avec un petit twist. les critiques ne serait pas celles de professionnels établit depuis des années, mais des gens du 'peuple', vous et moi et tous les autres.

### Ca existe déjà, non ?

J'ai conscience que de tels concepts ont déjà été testé et aprouvé, à différent niveaux de succès. Je souhaite le faire pour deux raisons: La première, comme précedement expliqué, cela n'existe pas vraiment en français, à ma connaissance.
La seconde est tout simplement l'opportunité d'apprendre différent aspect d'un même projet: l'aspect algorythmique, mais également l'aspect SysAdmin.

Après avoir lu une discussion à propos d'Amazon AWS sur HackerNews, j'ai réalisé que le projet pouvait non seulement être divisé en son code mais également dans son infrazstructure. J'essaierai donc quelques articles ayant pour sujet mes différentes explorations d'un solution, comment l'ensemble fonctionne, à la fois pour le code et pour les serveurs.

### Le Plan 

J'expliquerai plus en détails l'architecture du projet dans le prochain article. Je me conterai pour le moment de n'en donner qu'une vue aérienne.

L'idée est de recolter le plus possible de tweets à propos d'un film, de les aggrégés dans un liste, les analyser à l'aide d'un aglorithm d'analyse de sentiments, stocker les résultats dans une base de donnée, les complétes avec des informations classique (poster, date de sortie, ...) et finalement montrer les résultats finals à l'audience du site. 

J'espère à terme pouvoir automatiser l'ensemble le plus possible, et faire en sorte qu'il ne requiert que le minimum de maintenance. J'en suis encore loin.

Je travail actuelement sur le MVP (Minimum Viable Product), après plusieurs nuits sans sommeil à décider de quelle manière m'y prendre. J'ai décidé que si j'y passais ne serait-ce qu'une minute de plus à y réfléchir, je ne commencerai jamais à concrètement travailler dessus. Donc oui, pour l'instant c'est rudimentaire, plus proche d'une preuve-de-concept. Vous pouvez suivre l'avancement et y participer sur github [link].  

Dans les prochains articles, j'explorerai plus en details, et pas forcement dans cet ordre: l'architecture du projet, les différents élément d'AWS, les algorithms possible pour l'analyse, le fonctionnement de l'ensemble ...