# Le Risque


Bienvenue dans cette cinquième édition d'Investi! Aujourd'hui, on va parler du risque.

"La bourse, c'est risqué." Je ne compte plus le nombre de fois où j'ai entendu cette expression.
Mais qu'est-ce que ça veut dire en fait? Qu'est-ce que le risque en bourse? Comment le réduire? Est-ce que pour gagner plus d'argent, il faut prendre plus de risque?

Suivons le guide.

## Risque = possibilité de perte

Dans le monde des investissements, le risque est tout simplement la possibilité que tu peux perdre de l'argent. L'avenir des entreprises n'est pas certain, le comportement des participants sur les marchés n'est pas certain, et en particulier ton comportement n'est pas certain. Il se peut que la valeur des investissements que tu as fait en bourse soit inférieure à l'argent que tu y as investi. Le risque, c'est la possibilité de cette perte.

Note bien que ces considérations doivent être faites après taxation et inflation - c'est-à-dire, en termes de pouvoir d'achat. Dans la [lettre aux actionnaires de Berkshire Hathaway de 1980](https://www.berkshirehathaway.com/letters/1980.html), Warren Buffett fait en effet l'observation suivante:

Si tu:
- (a) renonces à dix hamburgers pour faire un investissement ; 
- (b) reçois des dividendes qui, après impôt, te permettent d'acheter deux hamburgers ; et 
- (c) lors de la vente de tes avoirs, tu reçois une somme après impôt qui te permettra d'acheter
huit hamburgers, alors
- (d) tu n'as eu aucun revenu réel de ton investissement, quelle que soit son appréciation en dollars.
Tu te sentiras peut-être plus riche, mais tu ne mangeras pas plus riche.

Le risque est donc la possibilité que ton investissement te fasse perdre du pouvoir d'achat. Très bien, mais comment mesurer tout ça?

## Définition académique du risque

Commençons d'abord par une définition académique du risque, et ce pour deux raisons:
- Cette définition est utilisée absolument partout, y compris dans les nombreux prospectus de produits financiers. C'est donc pratique à connaître.
- Elle est néanmoins très incomplète. Non pas en termes de formules (les théoriciens de la finance adoooorent les formules), mais en termes de bon sens paysan. C'est donc important d'en connaître les limites.

C'est parti.

Dans le monde de la finance, les théoriciens définissent le risque d'un actif comme la volatilité des fluctuations de son prix. Qu'est-ce que ça veut dire?

Disons que tu veilles mesurer le risque lié à l'action Microsoft. Un professeur de finance te dirait alors de regarder l'historique du prix de l'action à certains intervalles donnés (disons, à la clôture quotidienne des marchés). Tu devrais ensuite calculer la performance de l'action sur chacun de ces intervalles, pour en déduire une distribution de rendements. Le professeur te dirait alors de calculer ensuite la *variance* de cette distribution (un gros mot qui mesure à quel point ces rendements quotidiens sont dispersés).

On appelle cette variance *volatilité*. Dans le monde de la finance, c'est un des premiers chiffres qu'on te dirait de regarder. "*À quel point les rendements quotidiens de l'action Microsoft sont dispersés?*" devient une sorte de question de remplacement pour "*Quel est le risque lié à l'action Microsoft?*".

On va alors considérer qu'une action avec de faibles fluctuations est peu risquée, tandis qu'une action avec des fluctuations plus importantes est plus risquée.

![[peurisque.png]]

![[plusrisque.png]]

Mais ce n'est pas fini. En 1964, William Sharpe eut l'idée qu'on devrait comparer la volatilité d'une action à celle du reste du marché. Il ne suffit pas de savoir si le prix d'une action varie beaucoup, mais à quel point ce prix varie quand le marché fluctue. (Par "marché", on désigne en général la moyenne de toutes les entreprises cotées sur une place boursière particulière. On peut aussi prendre un indice représentatif de ce marché, comme le S&P500 aux USA ou le CAC40 en France.)

Je passe sur les formules, mais les calculs utilisés par Sharpe te donnent une grandeur appelée le *bêta*:
- Une action avec un bêta égal à 1 a tendance à varier autant que le marché
- Une action avec un bêta supérieur 1 a tendance à avoir des fluctuations plus importantes que celles du marché. On la considère donc comme plus risquée.
- Une action avec un bêta inférieur à 1 a tendance à avoir des fluctuations moins importantes que celles du marché. On la considère donc comme moins risquée.
- Une action avec un bêta négatif  a tendance à avoir des fluctuations inverses à celles du marché.

Toute la finance moderne repose sur ces deux notions de *volatilité* et de *bêta*. C'est très pratique, car avec seulement deux nombres on peut résumer tout le risque d'une compagnie. Un scientifique peut ensuite construire des modèles mathématiques élaborés à partir de ces concepts. 

## Une théorie limitée

La volatilité et le bêta sont certes très pratiques pour condenser l'information de risque, mais ces concepts ont de grosses limitations.

Tout d'abord, ils ne regardent que la performance passée d'une action. Celle-ci peut avoir un comportement totalement différent dans le futur.

Ensuite, la volatilité prend en compte les fluctuations à la baisse comme à la hausse. Je n'ai jamais vu quelqu'un ayant acheté les actions d'une compagnie venir se plaindre par la suite que la valeur de ses actions a augmenté. Si le risque est une possibilité de perte de pouvoir d'achat, pourquoi les fluctuations à la hausse sont-elles prises en compte?

Mais surtout, la volatilité et le bêta ne prennent jamais en compte le fait qu'une action est un titre de propriété sur une compagnie. Tu sais déjà que [sur le long terme, le cours d'une action suit la performance des profits de la compagnie](https://investi.cash/gains-en-bourse-connais-tu-les-regles-du-jeu/). Si les profits sont aussi déterminants dans la performance d'une action, pourquoi ne figurent-ils pas dans les mesures "classiques" de risque? Si une entreprise a une profitabilité décevante sur le long terme, ne s'agit-il pas d'un facteur de risque plus important que la volatilité de son action?

Comment réconcilier ces deux approches du risque?

L'analogie qui suit te permettra de mieux comprendre la relation entre ces deux mondes.

## Une histoire de promenade

Voici Alex et son chien, Tobby.

![[AlexTobby.png]]



Tous les matins, Alex part se promener avec Tobby dans le parc d'à côté. Alex est plutôt tranquille. Si on devait tracer sa trajectoire dans le parc, elle ressemblerait sûrement à ça:

![[AlexTrajectoire.png]]



Pour Tobby, c'est tout le contraire. C'est un jeune chiot, et il est tout excité! Quand Alex se promène, il fait de nombreux allers et retours autour de son maître.

![[AlexTobbyAvance.png]]


Si bien que si tu superposais la trajectoire d'Alex et Tobby dans le parc, ça donnerait quelque chose comme ça:

![[AlexTobbyTrajectoire.png]]
Mais ce n'est pas tout. Tobby est fasciné par les papillons. Quand il en croise un, Tobby devient fou et poursuit le papillon jusqu'à ce qu'il en perde la trace. Il retourne ensuite voir Alex. La trajectoire de Tobby diverge alors beaucoup de celle d'Alex.

![[AlexTobbyPapillon.png]]


Tu vois où je veux en venir. Si on devait faire le parallèle avec la bourse, Alex représenterait la compagnie et Tobby son action. Bien que la trajectoire de l'entreprise fluctue peu, le cours de son action va fluctuer autour de la valeur de l'entreprise.

Les papillons représentent les moments où les marchés deviennent particulièrement euphoriques ou pessimistes. Le papillon le plus à gauche serait alors une bulle spéculative et celui à droite un krach boursier.

Bien que cet exemple soit un peu simpliste, tu vas voir qu'on peut en tirer plein de leçons.

## Quand l'horizon se rétrécit

Imagine que l'on zoome sur un instant précis de la ballade. Alex n'aurait quasiment pas bougé, sa trajectoire étant bien rectiligne. Par contre Tobby pourrait être absolument partout - surtout s'il a vu un papillon. Au fur et à mesure que l'horizon temporel se rétrécit, les actions de Tobby ont très peu de rapport avec celles d'Alex.

En bourse, c'est la même chose. Sur une courte période, la valeur d'un business va très peu changer. Par contre le cours de son action peut beaucoup fluctuer! À court terme, il y a peu de rapport entre les deux. 
Étudier la compagnie ne permettra pas de prévoir le cours de son action. Dans ce cas, mesurer le risque en utilisant la volatilité et le bêta de l'action a pas mal de sens.

## À la fin, ce sont les bénéfices qui gagnent

Tu auras remarqué qu'à la fin de la ballade, Tobby sort toujours du parc avec Alex. Peu importe à quel point le chiot a été agité pendant la ballade. À la fin, Tobby rejoint toujours Alex pour sortir du parc.

Et en bourse, c'est aussi la même chose. Je l'ai déjà dit et je le répète encore: [sur le long terme, le cours d'une action suit toujours les bénéfices par action du business](https://investi.cash/gains-en-bourse-connais-tu-les-regles-du-jeu/). Plus ton horizon d'investissement s'allonge et plus les profits sont déterminants pour le cours de l'action. Dans ce cas là, la mesure la plus pertinente de risque est la trajectoire des profits. Si le business décline, tu peux être certain que ton investissement va prendre l'eau.

## Et les papillons?

Note enfin qu'on peut très bien utiliser ensemble la volatilité ET la connaissance du business pour analyser le risque d'une action. C'est en particulier très pertinent quand "Tobby poursuit les papillons".

Imagine que grâce à une bonne analyse, tu sais que la compagnie ABC va pouvoir croitre ses profits sur le long terme. Autrement dit, tu sais quelle sortie Tom va prendre pour sortir du parc et ça s'annonce plutôt bien. 

Par contre, aujourd'hui Tobby a décidé de poursuivre des papillons et il va à peu près partout dans le parc.

![[AlexTobbyPapillon 1.png]]

Revenons à la bourse. La sortie du parc représente la valeur de l'entreprise sur le long terme (et donc la valeur de son action). Grâce à ton analyse, tu as une bonne idée de sa valeur. Le premier papillon représente le premier épisode de volatilité: une bonne grosse bulle. Le prix de l'action devient extrêmement élevé. Même si la compagnie est promise à un avenir radieux, le prix de l'action à cet instant est tellement haut que la profitabilité du business ne pourra jamais le justifier. Acheter à ce moment serait un risque maximal: tu es quasiment certain de perdre de l'argent. Il n'existe pas de business qui soit si bon pour que l'on puisse se permettre de payer n'importe quel prix pour l'acquérir.

À l'inverse, le deuxième papillon représente un krach. Là aussi, beaucoup de volatilité. Par contre ici, c'est tout l'inverse: plus le prix est bas, plus tu es certain de gagner de l'argent! Dans ce cas, la volatilité ne représente pas un risque, mais une opportunité. 

C'est ce que raconte Buffett lorsqu'il conte son [acquisition du Washington Post](https://www8.gsb.columbia.edu/articles/columbia-business/superinvestors):

"En 1973, la société du Washington Post se vendait pour 80 millions de dollars sur le marché. À l'époque,  vous auriez pu vendre les actifs à n'importe lequel de dix acheteurs pour au moins 400 millions de dollars, et probablement beaucoup plus. La société possédait le Post, Newsweek, ainsi que plusieurs stations de télévision dans des marchés majeurs. Ces mêmes propriétés valent aujourd'hui 2 milliards de dollars, donc celui qui aurait payé 400 millions n'aurait pas été complètement fou." 

Maintenant, si l'action avait encore baissé à une valeur 40 millions au lieu de 80 millions de dollars, son bêta aurait augmenté. Et pour les personnes qui pensent que le bêta mesure le risque, un prix plus bas aurait fait paraître l'action plus risquée. C'est vraiment Alice au pays des merveilles. Je n'ai jamais réussi à comprendre pourquoi il est plus risqué d'acheter des propriétés d'une valeur de 400 millions de dollars pour 40 millions de dollars plutôt que pour 80 millions de dollars."


(*Oui, je cite beaucoup Warren Buffett. Oui, ça peut paraître cliché. Mais la qualité de ses lettres est telle que tu as beaucoup à gagner à lire ses textes.*)

## Quelques exemples:

Ok, assez parlé de promenades, il est temps de passer à des cas réels.
Le premier exemple est une compagnie canadienne dont voici l'historique du prix entre l'été 2015 et l'été 2016. Dirais-tu que cette action est risquée?

![[CSU1.png]]

Le cours est assez volatil, avec un plus haut aux alentours de 600$ et un plus bas d'à peu près 450$. Difficile de dégager une tendance. L'action ne semble pas très intéressante: pas mal de volatilité et un prix qui semble aller nulle part.

Si on prend du recul et qu'on regarde ce qu'il se passe sur 12 ans, l'histoire est bien différente. 

L'entreprise est Constellation Software, un éditeur de logiciels. Entre 2006 et 2022, Constellation a augmenté ses bénéfices par action de 35% par an. Sur le long terme, le prix a suivi. Lors de l'introduction en bourse en 2006 de Constellation Software, ses actions s'échangeaient autour de 15 dollars canadiens. Au moment où j'écris ces lignes en juillet 2022, le prix de l'action est de 1'993 dollars canadiens... 

Sur le graphe ci-dessous, le rectangle rouge correspond à la période mise en évidence dans le graphe précédent. Il y a trois leçons à tirer:
- À court terme, le prix d'une action peut faire n'importe quoi.
- Un an, c'est toujours du court terme.
- Un business ayant une performance remarquable sur le long terme déclenche toujours une performance remarquable du prix de son action.

![[CSU2.png]]


Passons à un deuxième exemple. En te basant uniquement sur le graphe ci-dessous, voudrais-tu investir dans ce business?

![[LTCM1.png]]

Faible volatilité, prix qui quadruple en quatre ans... Cet investissement a tout pour plaire! Grosse performance et faible risque (mesuré par sa volatilité). Où faut-il signer? Tout le monde voulait investir à l'époque.

Sauf que...
La compagnie en question était un fond d'investissement appelé Long Term Capital Management. Il employait entre autres deux prix Nobels d'économie, Robert Merton et Myron Scholes. Si tu as suivi des cours de finance, c'est le même Scholes que la formule de *Black-Scholes* pour déterminer le prix des options. 

Et pourtant, 6 mois plus tard, le fond faisait faillite.


![[LTCM.png]]

Le fond avait emprunté beaucoup d'argent pour tirer avantage de petites anomalies de marché. En 1998, l'effet de levier était de plus de 30-pour-1. Le levier magnifiait les profits, mais il se retourna rapidement contre la compagnie quand les marchés eurent un comportement inattendu et que le fond subit de lourdes pertes. 

Ici encore, quelques leçons à tirer:
- Une faible volatilité du prix de l'action ne protège pas des risques inhérents au business. Ici le risque principal résidait dans l'effet de levier beaucoup trop important pour la compagnie.
- Les prix Nobels n'empêchent pas de faire faillite. Merton et Scholes avaient certes créé une performance remarquable avec une très faible volatilité pendant quatre ans. Ça n'empêche pas qu'une action est bien plus qu'une courbe sur un graphe. Mesurer le risque uniquement avec la volatilité peut te mettre dans des situations très inconfortables.
- **Emprunter de l'argent et utiliser l'effet de levier transforme la volatilité à court terme en risque de pertes à long terme.**


## Le risque pour l'investisseur sur le long terme

À ce stade, tu as compris que la définition académique du risque n'est valide que sur du court terme. 
Si tu as un horizon d'investissement plus long, le risque est surtout que les profits que ton business va générer soient décevants par rapport au prix que tu as payé pour la compagnie. Là encore, Buffett vient confirmer cette vision du risque.

Dans sa [lettre aux actionnaires de Berkshire Hathaway de 1993](https://www.berkshirehathaway.com/letters/1993.html), il écrit:


À notre avis, le véritable risque qu'un investisseur doit évaluer est de savoir si ses recettes totales après impôts provenant d'un investissement (y compris celles qu'il perçoit lors de la vente) lui donneront, au cours de la période de détention envisagée, un pouvoir d'achat au moins égal à celui qu'il avait au départ, plus un taux d'intérêt modeste sur cette mise initiale.

Bien que ce risque ne puisse être calculé avec la précision d'un ingénieur, il peut dans certains cas être jugé avec un degré de sensibilité qui reste utile. Les principaux facteurs qui influent cette évaluation sont:

1) La certitude avec laquelle les caractéristiques économiques à long terme de l'entreprise peuvent être évaluées.
2) La certitude avec laquelle l'équipe direction peut être évaluée, tant en ce qui concerne sa capacité à réaliser le plein potentiel de l'entreprise qu'à utiliser judicieusement ses flux de trésorerie.
3) La certitude avec laquelle on peut compter sur l'équipe de direction pour canaliser les bénéfices de l'entreprise vers les actionnaires plutôt que vers elle-même.
4) Le prix d'achat de l'entreprise 
5) Les niveaux d'imposition et d'inflation atteints qui détermineront dans quelle mesure le rendement du pouvoir d'achat d'un investisseur est réduit par rapport à son rendement brut. 

Ces facteurs paraîtront probablement insupportablement flous à de nombreux analystes, car ils ne peuvent être extraits d'une quelconque base de données. Mais la difficulté de quantifier précisément ces questions ne nie pas leur importance et n'est pas insurmontable. De même que le juge Stewart estimait qu'il était impossible de formuler un critère d'obscénité mais affirma néanmoins : "Je le sais quand je le vois", de même les investisseurs peuvent - d'une manière inexacte mais utile - "voir" les risques inhérents à certains investissements sans se référer à des équations complexes ou à l'historique des prix.

Dans ces quelques paragraphes résident tout ce que tu dois savoir quant aux risques que tu dois évaluer:
- Ne pas pouvoir évaluer l'avenir économique d'une entreprise, c'est risqué.
- Ne pas savoir si les directeurs de l'entreprise sont compétents pour exécuter leur stratégie (ou si leur stratégie est pertinente), c'est risqué.
- Ne pas savoir si l'équipe de direction réinvestira correctement le cash généré par l'entreprise, c'est risqué.
- Ne pas savoir si le directeur est plus intéressé par son enrichissement personnel que par sa responsabilité vis-à-vis des actionnaires, c'est risqué.
- Acheter un business pour plus que ce qu'il ne vaut, c'est excessivement risqué.
- Acheter un business dont la profitabilité ne pourra pas atténuer les effets de l'inflation, c'est risqué.

Oui, toutes ces notions sont purement qualitatives. Contrairement à la volatilité et au bêta, ce ne sont pas des nombres concrets que tu peux ensuite insérer dans des formules. Mais cela n'enlève rien à leur importance. Comme disait Einstein, "*Ce qui compte ne peut pas toujours être compté, et ce qui peut être compté ne compte pas forcément*". Ces facteurs comptent énormément et on ne peut pas les compter ou les résumer à un simple nombre.

Si on va jusqu'au bout de la pensée de Buffett, **le job d'un investisseur est alors de *réduire le risque***.  Paradoxalement, plus un investisseur limite les facteurs de risque (un business de qualité, prévisible, avec une équipe de direction compétente et intègre, peu touché par l'inflation et disponible à un prix raisonnable), plus il a de chances de gagner de l'argent.

**On renverse complètement les paradigmes de base de la finance moderne. On passe de "Pour gagner plus d'argent, prends plus de risques" à "Pour gagner plus d'argent, réduis le risque au minimum."** Un gros choc des cultures...

## Conclusion

C'est tout pour aujourd'hui. Voici les points à retenir:
- Le risque, c'est la possibilité de perdre du pouvoir d'achat à cause de ton investissement.
- Bien que le monde académique définisse le risque comme la volatilité du cours d'une action (et de comment cette volatilité évolue par rapport au reste du marché), cette définition est très incomplète et ne convient qu'à court terme.
- Si tu es un investisseur à long terme: le risque, c'est quand le business dans lequel tu as investi génère des bénéfices décevants par rapport à ce que tu as payé.
- En particulier, chacun des points suivants augmentent le risque de ton investissement:
	- Plus il est difficile d'avoir une image réaliste des futurs profits du business, plus l'investissement est risqué.
	- Moins l'équipe de direction est compétente pour exécuter la stratégie du business et allouer son capital, plus l'investissement est risqué.
	- Plus les intérêts de l'équipe de direction sont éloignés de ceux des actionnaires, plus l'investissement est risqué.
	- Plus tu payes un prix élevé pour ton business, plus l'investissement est risqué.
	- Plus le business est vulnérable à l'inflation, plus l'investissement est risqué.


On creusera tous ces points en détails dans de futures éditions d'Investi. En attendant, à la semaine prochaine!










