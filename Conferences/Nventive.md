#### Trade Zero
Données en temps réel: moteur d'une application mobile ultra-performante

#### Contact: Jean-Philippe Lévesque
9 ans chez Nventive

C# depuis 2008 (lionel groulx?)

Trade zero client de Nventive
plateforme sans commission

Motivation de TradeZero: GME, RobinHood, Webull

Il croit que la demande est là

TradeMobile a des widgets?

Nventive a développer le feature des hotkeys afin de pré-remplir les formulaires afin d'accélérer le processus d'achat/vente/short
Permet de rapidement envoyer des commandes

Short: ta perte est infini

Ils ont ré-utiliser l'ancienne palteforme ils ont garder le back-end pour la communication au serveur en temps réel, les graphiques etc

#### Technologies: .Net, Uno Platform, Xamarin, C#, XAML, Archi MVVM

SkiaSharp, C# wrapper

#### Open source
Ils ont publiés leurs lib comme:
BiometryService: détect le os du mobile 

Environnement .Net

données encapsulé dans des libs TradeZero

### 1st Problem data access
they mocked the data to start the UI/UX and validate the designs and navigation etc

Perfect for testing because the stock market is only open from 9:30 to 16:00 so it allowed Nventive to work on the platform whenever they wanted




### 2nd Problem high data flow
Le grand débit de données
La simulation de données n'étaient pas assez aggressives
La performance de l'application était affectée, lag, freeze, etc
#### Solution - Optimisation 
Dispatcher Batching
Optimisation lié au UI Thread
Réduire la charge de travail associé au UI



Afin de calmer le flux de données, ils désabonnent le flux de données des éléments qui ne sont pas présentement observé. Cela permet d'optimiser la consommation de ressource en arrière-plan et au UI Thread.

### What they learned
Not hesitate to develop toold to help and simplify developpment
Understand the implications of real-time apps (you can ignore informations, update less frequently like 5 ms less)

Services subscription

## Open Source App templates
Login de fait
des logs
des pipelines
déploiement
tests automatisés
enterprise ready
everything ready

ils ont 58 repos open source
des templates d'app mobile
https://github.com/nventive

https://github.com/nventive/UnoApplicationTemplate