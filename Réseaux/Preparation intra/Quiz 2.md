### Question 1. 
Commutateur 24 ports. Tous les ports du commutateur sont configurés en mode dynamique afin de bâtir la table de communication.
#### a) 
Si la table est vide est une trame avec l'adresse MAC de DA est 0C et la SA est 0F est transmise au commutateur, indiquez si les énoncés du tableau 1 sont vrais ou faux.
![[Pasted image 20231016152914.png]]
Le commutateur va ajouter l'adresse MAC de la source 0F avec le port associé (port 21) dans sa table de communication.
#Vrai

Le commutateur va ajouter l'adresse MAC de la destination 0C avec le port associé (port 9) dans sa table de communication.
#Faux, il ne connaît pas le port associé à la destination 0C

La commutateur va jeté la trame.
#Faux 

Le commutateur va transmettre la trame uniquement sur le port 9 pour atteindre la destination.
#Faux 

Le commutateur va transmettre la trame sur tous ses ports "actifs" sauf le port 21 sur lequel il a reçu la trame.
#Vrai 
#### b) 
Considérons la table de communication et une trame avec DA = 0B et SA = 0E est transmise au commutateur. Indiquez les énoncés vrais et faux. 
(Chaque entrée est inscrite pendant 1800 secondes)
![[Pasted image 20231016152936.png]]

*Résumé de la situation*: 
Le port 0E nous dit d'envoyer qqch à 0B.
La source 0E, n'est pas dans la table, alors on va l'ajouter.
La destination 0B est inscrite dans la table au port 5, alors on va envoyé notre truc seulement au port 5.
Fin.

Le commutateur va ajouter SA = 0E avec le port 17 associé à sa table.
#Vrai 
Le commutateur va ajouter DA = 0B avec le port 5 associé à sa table.
#Faux 
Le commutateur va rejeter la trame.
#Faux 
Le commutateur va transmettre la trame uniquement sur le port 5 pour atteindre la DA.
#Vrai 
Le commutateur va transmettre la trame sur tous ses ports actifs saufe la SA.
#Faux 

### Question 2
Est-ce que la technologie IP:

a) utilise la commutation de paquets?
#Vrai 
b) utilise des paquets dont la longueur est variable?
#Vrai 
c) offre un service sans connexion?
#Vrai 
d) offre un service avec une qualité de service garantie?
#Faux 
### Question 3
Une petite entreprise décide d'utiliser l'adresse 192.168.20.0/24 pour son réseau.
Elle a besoin de 4 sous-réseaux pour 4 départements: 1) ingénierie, 2) production, 3) comptabilité et R.H., 4) marketing et distribution. Le nombre de postes de travail dans chacun de ces sous-réseaux est respectivement 25, 20, 15, 28.
![[Pasted image 20231016154421.png]]
#### a)
Proposez un masque de sous-réseau pour satisfaire ces contraintes et assignez des adresses aux sous-réseau.

???????????????????????????????????????

#### b)
Quel est l'espace des adresses restantes?

**Si le routeur a une adresse on fait -1, car c'est le gateway par défaut**

Pour le département 1 on a besoin de 25 postes de travail.
On utilise 192 on a donc 62 hôtes par sous-réseau
Alors ça sera: 62 - 25 = 37

pour le dép 2 besoin 20 alors 62-20 = 42
pour le dép 3 besoin 15 alors 62-15 = 47
pour le dép 4 besoin 28 alors 62-28 = 34

#### c)
Quelles informations supplémentaires faudrait-il pour déterminer la meilleure solution en a)?
Dans le cas où un département se divise, il serait préferable de prendre directement 3 bits pour le host id.

### Question 4
![[Pasted image 20231016160313.png]]

#### a) 
Si un paquet arrive au routeur avec l'adresse IP de destination 172.24.100.2, quelle sera sa sortie?
Interface 1
#### b) 
Si un paquet arrive au routeur avec l'adresse IP de destination 126.15.50.1, quelle sera sa sortie?
Interface 6
#### c) 
Si un paquet arrive au routeur avec l'adresse IP de destination 172.24.10.5, quelle sera sa sortie?
Interface 3

### Question 5
Quel est le danger de mesurer la fiabilité d'un réseau que par la connexité? Donnez un exemple.

On ne tient pas compte de la capacité du réseau. Il faut regarder la performance pour éviter la congestion.

### Question 6
Considérons l'utilisation d'une application de vidéoconférence. Une vidéo en couleur numérique est une série d'images consistant chacune en une grille de pixels. Pour obtenir un mouvement fluide, 25 images doivent être affichées par seconde. 
- Chaque image vidéo contient 1280 x 720 pixels
- la représentation d'un pixel est de 3 octets
- le ratio de compression est de 50:1
- la sommes des entêtes et de l'espace intertrame ("*InterPacket Gap*") est 78 octets
- les paquets contiennent normalement 1000 octets de données vidéo

a) Calculez la taille en octets d'une image compressée.
1280x720 = 921 600 pixels pour 1 image
921 600 x 3 octets = 2 764 800 octets pour 1 image
2 764 800 octets/50 = 55 296 octets

**55 296 octets après compression**

b) Calculez le nombre de paquets par seconde pour transmettre une vidéo compressée.

55 296 octets/image / 1000 octets/paquet = 55,296 ~ 56 paquets/image
56 paquets/image x 25 images = 1400

**1400 paquets**

c) Calculez le débit au niveau de la couche physique pour transmettre une vidéo compressée,
T = taille
Débit = n bit/octet x n image x (T_paquet + T_IPG) 

= {55 paquets x (1000+78)x8 + 1 paquet x (296+78)x8} x 25
(Car on a pour 55,296 paquets à envoyer. On a 55 paquets de taille = 1000 octets et 1 paquet de taille = 0,296 octets)

= 11 932 800 bits par seconde

= 11, 933 M bits ps

= 11, 933 Mbps