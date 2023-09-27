faute dans ses diapos? ALHOA* => ALOHA 
oui il a fait une faute, lui dire


Les protocoles IEEE 802.x couvrent les couches Physique et
Liaison du modèle OSI

![[Pasted image 20230927095255.png]]

SNAP: Service Network Protocl Access Point

Lorsqu'on parle de splanning tree ils utilisent tous l'encapsulation 802.2

![[Pasted image 20230927100226.png]]

Diapo 26

### Questions
• Quel doit être le temps de détection minimum ?

Combien de temps on doit ecouter avant d'envoyer nos shits?

I : delai de propa

on doit ecouter pendant 2 x I (2 fois le delai de propa)

Le temps de detection minimal = 2xI

• Pourquoi utiliser une séquence de brouillage (32 bits) ?

Pour eviter une collision, on avertit les autres stations qu'on a detecter une collision

![[Pasted image 20230927103620.png]]


![[Pasted image 20230927103642.png]]

![[Pasted image 20230927104021.png]]




Ce qu'on utilise
![[Pasted image 20230927104221.png]]

Utiliser pour communiquer de l'info entre les commutateurs et pour les splanning trees
![[Pasted image 20230927104316.png]]

![[Pasted image 20230927104543.png]]

Si on a des paquets a transmettre on va prendre Trame Ethernet II

### Exercice avec 2 commutateurs

![[Pasted image 20230927105502.png]]

#### a)
- trame arrive au port 1
- commutateur regarde l'addresse de destination
- transmettre la trame sur tous ses ports actifs c-a-d 4 ensuite 3 dans cet ordre
- B va recevoir sa trame
- la trame arrive sur le port 1
- commut regarde laddr de destination
- va a la passerelle de niveau

c'est pas smart les commutateurs, cela envoi 

#### b)

#### c)

pas fait, mais il dit que ce sont les meme regles a suivre

-----------------------


Si on veux separer les domaines de broadcoast il faut un routeur
p.50

Il y a beaucoup de duplicats et de redondances dans les reseaux, car on souhaite que le reseau demeure operationnel lors d'une panne ou lors d'un entretien technique

![[Pasted image 20230927110331.png]]


### Exercice
![[Pasted image 20230927110552.png]]

#### a)
- on envoit la trame a C1
- la table est vide alors on envoit la trame a tous les ports actifs
- C2 et C3 recoivent la trame
- ils vont l'envoyer sur tous leurs ports
- la trame va arriver au port 4 et le pc B va reconnaitre l'adresse de destination comme etant la sienne

B va le recevoir une infinite de fois car la boucle que forme C1, C2, C3 la trame va tourner indefinitivement


le splanning tree sert a desactiver les ports inactifs
#### b)
p.55
![[Pasted image 20230927110949.png]]

#### d) 
les problemes vont ressembler a ceux dans a/b



